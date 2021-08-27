# App Reg Best Practice for Azure Functions that act as API

``Configuration example on Premium plan, but similar config is also possible with consumption, with different GUI options `` 

- [App Reg Best Practice for Azure Functions that act as API](#app-reg-best-practice-for-azure-functions-that-act-as-api)
  - [Creation](#creation)
  - [Hardening](#hardening)
    - [Assignment](#assignment)

1. Remove redirect URI's (If you are creating a new function, select the api scheme HTTP401 for unauthenticated requests)
2. Remove Token Store, as there is no need to store tokens for client credential flow based clients ,
3. Require user assignment, so arbitrary token issuance is not enabled for anonymous app registrations 


## Creation
![img](img/appreg.png)

`` - There is no need for redirect URI, as the caller already has the access token, at the time it calls the api``  

## Hardening 
![img](img/hardening.png)

### Assignment 
![img](img/assignment.png)

