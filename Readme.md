# Goals

Google is removing its free tier from the Google Apps/GSuite/Workspace product making it prohibitively expensive for families, prosumers, and small business who just want to use gmail with custom domain names and don't need expansive capabilities Google Workspace provides to enterprises.

Historically Google marketed GSuite (Google Apps back then) as a tool for families and small organizations. Many early adopters are using their GSuite Google account for more than ten years and accumulated digital legacy they do not want to loose. Many of these people were early adopters of many other Google technologies: Android, Google Talk, Google Reader, Google Docs, Google Voice, Inbox, Wave, Google Cloud, Google Pay to name a few. Unfortunately, Google provided no tools for early GSuite adopters to migrate their accounts to "normal" free Google accounts, demanding a lifetime ransom for people's digital live.

If a GSuite account remains unpaid Google will convert the account to a "Google Identity". This is a incomplete Google account which does not include Gmail and Calendar (but for some reason includes Google Drive). While many Google services work with Google Identity its usage is inconvenient as one will be requited to be logged in into several account to use free Gmail and former GSuite Google Photos for example. Google identity are known not to work with Google Pay and Google One.

This guide aims to document a migration process out of GSuite Google accounts to free Google accounts.

# Migration

|Service|Migratable?| Action | Migration tools|Cloud Identity| Notes|
|---|---|---|---|---|--|
|Gmail| Y |Copy all emails from gsuite account a new Gmail account  | GYB | N|Will labels be copied as well? Can be very slow
|Gmail - rules| Y| Recreate rules in a new account| Manual| N |
|Google Talk (Hangouts)| N|Chat history cannot be migrated and will be lost |None | N | This is sad
|Google Drive| Y|(I migrated to Syncthing long time ago)| |Y | N/A 
Google Calendar | Y | Share all calendars with a new account | Manual | N | Painful for shared calendars
|Google Play| N|N/A|N/A| Y| Some Google Movie purchases can be exported via MoviesEverywhere
Google Contacts | Y | Export to csv, import in a new account| Manual| N
|Google Photos |Y| Add a free Gmail account as a partner from the Gsuite side and then save all pictures from the Gmail account side | partner account | Y | Untested. Another option is to download and re-upload everything via Google Takeout
Google Keep| N | Copy important notes manually | Manual| ?? | C'mon Google!
|Google Pay|N | All cards need to be re-added| Manual| N | Thanks!
|Google Maps - Favorite places| Y| Favorite places can be copied manually| Manual| Y | Painful if many
|Google Maps - Contributions| N| N/A|N/A| ? | Untested
YouTube - subscriptions| N | N/A | N/A | Y |Just resubscribe to your favorite channels
YouTube - channels| Y | ??? | ??? | Y | Untested
Google Cloud| ? |?|?|Y|More info needed
Google Home|N | N/A | N/A| N | Google Home never worked well with Gsuite
Google Storage| N | Ask for refund? Repurchase Google One | N/A | Y 
Google Scholar| N | Not supported by Google | N/A | ??
Google Groups | ? | (I don't use) |N/A|?
Google Analytics | Y | Use provided migration tool | Built-in | ?? |
Google Timelines | N | Can be exported via Takeout, cannot be imported | N/A | Y | This is sad
Google Authenticator| Y | Scan QR codes for each token  | Manual | ?? | 
Google OAuth | N | N/A | N/A | Y 





# Execution Plan


  - [ ] Register a non-Gmail account if you do not have one. There are plenty of providers out there, live360, zoho, aol, etc. This account will be used for an email forwarder registration, gmail recovery, and other critical stuff. In general, you should not give this account to other people.
  - [ ] Register a GMail account your are going to migrate to. It is better if the account exists for some time before you start messing around with transition.
  - [ ] Gmail clean up. The less stuff you need to move between accounts - the better.
    - [ ] Delete old emails you do not care anymore. Notifications from social media, promo codes circa 2011, etc, this adds up to tens of thousands of emails. Use gmail filters to delete them from the GSuite account.
    - [ ] Look for large attachments you don't need to carry over. Delete theese emails.
    - [ ] Delete irrelevant contacts.
  - [ ] Register for Cloudfare. Use the non-Gmail email for registration.
  - [ ] Ask for email forwarder beta.
  - [ ] Transfer your domain Cloundfare. For now preserve Google MX records
  - [ ] Register for an smtp forwarder (i.e. mxroute). This costs money. I see it as a temporary solution until (i) Cloudfare creates such service (ii) good self-hosted solution emerges (unlikely)








