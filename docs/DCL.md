Use Case: Restrict the Value help of the standard CDS view with particular values like z*. Instead of showing all the values in the Value help

1. Create Authorization Class(ZOTC), Authorization Object(ZOTC_RJCN) and add the Authorization Field(ZRJCN)
   ![image](https://github.com/govendrana/kodiak/assets/169263393/7b8227fc-2cac-4b24-b400-72fd339535d6)

2. Add the Authorization Field in SU24 by creating variant for the standard service
   ![image](https://github.com/govendrana/kodiak/assets/169263393/7b81dfc9-79ff-4df4-9a7b-56b5fd76c61e)

3. Under Menu -> Authorizatin Default -> 19 SAP Gateway Business Suite Enablement - Service. Add the standard service to the role
   ![image](https://github.com/govendrana/kodiak/assets/169263393/a7bb2092-dc93-49b5-ac3d-77f5e1f950b8)
   ![image](https://github.com/govendrana/kodiak/assets/169263393/dd909e1e-3a94-4c26-b922-9e1795ffca53)

4. Under Application -> Activate the variant of the standard service
   ![image](https://github.com/govendrana/kodiak/assets/169263393/9eba60fe-a5c6-4a7b-b471-989935e9c6f4)

5. Authorization -> Change Authorization data. Custom Authorizatin object will be visible in the role after the standard authorization object.
   Assign the ABGRU(Rejection Code as Z*)
   Assign the role to the User
   ![image](https://github.com/govendrana/kodiak/assets/169263393/a5cea437-005d-4929-9bab-4aa0d4d3ef18)

6. Find the corresponding CDS View
      -> Authorization Check is not required. But roles can be defined for later on
   ![image](https://github.com/govendrana/kodiak/assets/169263393/709333e0-895e-464e-b67f-d24c85a1d06a)

7. Create a custom DCL for the standard Value help CDS View and add the custom authorization object fielt to it. 
   ![image](https://github.com/govendrana/kodiak/assets/169263393/e3368e2c-c8c9-4fca-80aa-26d1c795736b)

8. Run the app. Value help will be restricted with only Z* for the user
   ![image](https://github.com/govendrana/kodiak/assets/169263393/d863c124-a272-439f-9826-b393bb59be07)

9. STAUTHTRACE – Authorization object is captured in trace while using the app
   ![image](https://github.com/govendrana/kodiak/assets/169263393/af2d1bf0-acb9-4165-8f2f-054491f23447)


