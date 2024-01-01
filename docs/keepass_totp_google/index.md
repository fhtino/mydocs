---
layout: doc
categories: docs
publish_date: 2022-07-18
---

# Using KeePass as a 2-step sign-in method with Google accounts

This post is about using KeePass with Google account for the 2-step verification process.

General considerations about using KeePass as a storage for TOTP keys and generator of one-time-password, can be found <strong> ==> [here]({% link docs/keepass_totp_intro/index.md %}) <== </strong>:


The following steps assume the 2-step-verification has been already activated. If not active, some more steps are required. But the fundamental ones are the same.

With a Google account, login to <https://myaccount.google.com/> and select Security:

<myimage><img src="1.jpg" width="400px"></myimage>

Select 2-Step verification details:

<myimage><img src="2.jpg" width="500px"></myimage>

If an authenticator is already registered, it is impossible to generate a new key. The old one must be removed and a new one created. Select the details of authenticator app:

<myimage><img src="3.jpg" width="400px"></myimage> 

Remove the current authenticator app. **Important:** before doing that, be sure to have activate another authentication method like "phone SMS" and "backup codes".

<myimage><img src="4.jpg" width="400px"></myimage> 

Add a new authenticator app:

<myimage><img src="5.jpg" width="500px"></myimage> 

Google generates a new random TOTP key and embeds it into a datamatrix. This is very useful for auto-registering the Authenticator but, for now, press "Can't scan it?"

<myimage><img src="6.jpg" width="400px"></myimage> 

Now the secret key appears as plain text:

<myimage><img src="7.jpg" width="400px"></myimage> 

Copy and paste the value inside KeePass:

<myimage><img src="8.jpg" width="400px"></myimage>  

<myimage><img src="9.jpg" width="350px"></myimage> 

Remove the white spaces and leave the other values empty (default values). If everything is correct, KeePass immediately starts generating OTP values. Press OK

<myimage><img src="10.jpg" width="350px"></myimage>  

Now, press "back" in the browser for coming back to the datamatrix. From the mobile Authenticator app, scan the datamatrix. Now the mobile Authenticator app and KeePass are generating the same one-time-password code, as expected.

Press "next" in the browser and enter the generated code:

<myimage><img src="11.jpg" width="400px"></myimage> 

Now the Authenticator app and KeePass are ready to be used.

<myimage><img src="12.jpg" width="400px"></myimage>  

For obtaining an OTP code from KeePass, right click the entry -> other data -> copy time-based otp. Paste it where required.

<myimage><img src="13.jpg" width="450px"></myimage> 

 
 