# Backend Coding Challenge: Module Dependency Challenge

### ProjectStructure
This Spring-Boot-Project consists of three Submodules (`inquiry`, `notification` and `application`).
The `notification`-Module depends on the `inquiry`-Module. The `application` depends on both and serves as Spring boot main module.

The `InquiryTest` calls `InquiryService#create(Inquiry)` and checks wether the methods `EmailHandler#sendEmail(Inquiry)`
and `PushNotificationHandler#sendNotification` have been called with the same parameters.

### Acceptance Criteria: 
- After an Inquiry has been created, `EmailHandler#sendEmail(Inquiry)` and `PushNotificationHandler#sendNotification` have to be executed
- the `InquiryTest` has to be successful
 
### general conditions:
- the classes `Inquiry`, `InquiryTest` and `Application` shall not be modified
- the existing classes shall not be moved between the modules
- the dependencies between the modules shall not be customized
- Any other gradle dependencies can be added
