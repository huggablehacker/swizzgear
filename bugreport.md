#### Issue description
There is an vulnerability in the `"SwizzGearPass"` mobile app, Specifically in how the app handles authentication of devices. I’ve seen and tested that the app does not have a mechanism to validate additional devices added to a particular account. This can lead to multiple riders using the same account to ride. This seems to be limited to three changes, but the core issue of multiple devices per account is the point of focus. 

#### Steps to reproduce the issue

1. Download `SwizzGearPass App` from the `Google Play` or `Apple App Store` 
2. Log into device using valid credentials. (Phone Number, MFA code, and Personal Pin) --  Side Note: Using SMS as MFA is also a potential issue, as SMS can be co-opted.
3. Both devices now display the same account with access to all available passes

#### Additional details / screenshots

- ![Screenshot]()
-


#### Potential Fixes

- Create some type of device validation in the code that would disallow multiple devices logging in form the same credentials. 
- Having fare enforcement use a validation system that creates a `temporary` lockout on accounts for a few minutes to prevent multiple people from using the same ticket on the app within a set time. 
