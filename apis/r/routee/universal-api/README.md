# <img src="https://images.mindcloud.co/apps/icons/routee_1775498966229.png" alt="Routee logo" width="28" height="28"> Routee: Universal API

Routee is a communication platform for SMS, verification, failover, contact, lookup, validation, URL, and account workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/routee/latest
- **Category:** Communication / Team Messaging
- **Actions:** 188
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://routee.net
- **Vendor API docs:** https://docs.routee.net/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check Account Balance](actions/check-account-balance.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/routee/latest/actions/check-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (188)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Get pricing for all Routee Services](actions/get-pricing-for-all-routee-services.md) | GET | Retrieves pricing for all Routee services. |
| [Get your account transactions](actions/get-your-account-transactions.md) | GET | Retrieves your current Routee account transactions. |

### Contacts

| Action | Method | Description |
| --- | --- | --- |
| [Add Contacts to a specified group](actions/add-contacts-to-a-specified-group.md) | POST | Adds contacts to a specified group in Routee. |
| [Add contacts to blacklist](actions/add-contacts-to-blacklist.md) | POST | Adds contacts to the blacklist in Routee. |
| [Create a new contact](actions/create-a-new-contact.md) | POST | Creates a new contact in Routee. |
| [Create a new group](actions/create-a-new-group.md) | POST | Creates a new group in Routee. |
| [Create group from difference](actions/create-group-from-difference.md) | POST | Creates group from difference in Routee. |
| [Create Labels](actions/create-labels.md) | POST | Creates new contact labels in Routee. |
| [Delete a contact](actions/delete-a-contact.md) | DELETE | Deletes an existing contact from Routee. |
| [Delete Groups](actions/delete-groups.md) | DELETE | Deletes existing groups from your Routee account. |
| [Delete multiple contacts](actions/delete-multiple-contacts.md) | DELETE | Deletes multiple contacts from your Routee account. |
| [Get blacklisted contacts for service](actions/get-blacklisted-contacts-for-service.md) | GET | Retrieves blacklisted contacts for service from Routee. |
| [Merge multiple groups](actions/merge-multiple-groups.md) | PUT | Merges multiple groups in your Routee account. |
| [Remove a group of contacts from the blacklist](actions/remove-a-group-of-contacts-from-the-blacklist.md) | DELETE | Removes a group of contacts from the blacklist in Routee. |
| [Remove Contacts from blacklist](actions/remove-contacts-from-blacklist.md) | DELETE | Removes contacts from the blacklist in Routee. |
| [Remove Contacts of a specified group](actions/remove-contacts-of-a-specified-group.md) | DELETE | Removes contacts of a specified group in Routee. |
| [Retrieve all the contacts](actions/retrieve-all-the-contacts.md) | GET | Retrieves all the contacts from Routee. |
| [Retrieve details about a contact](actions/retrieve-details-about-a-contact.md) | GET | Retrieves details about a contact from Routee. |
| [Retrieve one of the account's groups](actions/retrieve-one-of-the-accounts-groups.md) | GET | Retrieves one of the account's groups from Routee. |
| [Retrieve the account's contact labels](actions/retrieve-the-accounts-contact-labels.md) | GET | Retrieves the account's contact labels from Routee. |
| [Retrieve the account's groups](actions/retrieve-the-accounts-groups.md) | GET | Retrieves the account's groups from Routee. |
| [Retrieve the account's groups in paged format](actions/retrieve-the-accounts-groups-in-paged-format.md) | GET | Retrieves the account's groups in paged format from Routee. |
| [Update a contact's details](actions/update-a-contacts-details.md) | PUT | Updates a contact's details in Routee. |
| [View the Contacts of a specified group](actions/view-the-contacts-of-a-specified-group.md) | GET | Retrieves the contacts of a specified group from Routee. |

### Email Api V1 / Addresses

| Action | Method | Description |
| --- | --- | --- |
| [Change Variable for an Email Contact](actions/change-variable-for-an-email-contact.md) | POST | Changes a variable for an email contact in Routee. |
| [Erase an email address from all mailing lists](actions/erase-an-email-address-from-all-mailing-lists.md) | DELETE | Deletes an email address from all mailing lists in Routee. |
| [Retrieve detail information about a specific email address](actions/retrieve-detail-information-about-a-specific-email-address.md) | GET | Retrieves detail information about a specific email address from Routee. |
| [Retrieve general information about bulk of email address](actions/retrieve-general-information-about-bulk-of-email-address.md) | GET | Retrieves general information about bulk of email address from Routee. |
| [Retrieve general information for a specific email address](actions/retrieve-general-information-for-a-specific-email-address.md) | GET | Retrieves general information for a specific email address from Routee. |
| [Retrieve statistics for an email address by campaigns](actions/retrieve-statistics-for-an-email-address-by-campaigns.md) | GET | Retrieves statistics for an email address by campaigns from Routee. |
| [Retrieve statistics for email addresses by campaigns and presence in lists](actions/retrieve-statistics-for-email-addresses-by-campaigns-and-presence-in-lists.md) | POST | Retrieves statistics for email addresses by campaigns and presence in lists from Routee. |

### Email Api V1 / Blacklist / Balance

| Action | Method | Description |
| --- | --- | --- |
| [Blacklisting an email address](actions/blacklisting-an-email-address.md) | POST | Adds an email address to the Routee blacklist. |
| [Check the user’s balance](actions/check-the-users-balance.md) | GET | Retrieves the current user balance from Routee. |
| [Detailed balance info](actions/detailed-balance-info.md) | GET | Retrieves detailed balance information from Routee. |
| [Erase an email address from the blacklist](actions/erase-an-email-address-from-the-blacklist.md) | DELETE | Deletes an email address from the blacklist in Routee. |
| [Unsubscribe contact from the defined mailing list](actions/unsubscribe-contact-from-the-defined-mailing-list.md) | GET | Unsubscribes a contact from a Routee mailing list. |
| [View the blacklist](actions/view-the-blacklist.md) | GET | Retrieves the current blacklist from Routee. |

### Email Api V1 / Campaigns/templates

| Action | Method | Description |
| --- | --- | --- |
| [Campaign information](actions/campaign-information.md) | GET | Retrieves detailed campaign information from Routee. |
| [Cancel a campaign](actions/cancel-a-campaign.md) | DELETE | Cancels an existing campaign in Routee. |
| [Country statistics](actions/country-statistics.md) | GET | Retrieves detailed country statistics from Routee. |
| [Create a campaign](actions/create-a-campaign.md) | POST | Creates a new campaign in Routee. |
| [Edit planned campaign](actions/edit-planned-campaign.md) | PUT | Updates an existing planned campaign in Routee. |
| [Edit template](actions/edit-template.md) | PUT | Updates an existing template in Routee. |
| [Get info about template](actions/get-info-about-template.md) | GET | Retrieves info about template from Routee. |
| [Referrals statistics](actions/referrals-statistics.md) | GET | Retrieves detailed referrals statistics from Routee. |
| [Retrieve a list of all templates in the account](actions/retrieve-a-list-of-all-templates-in-the-account.md) | GET | Retrieves a list of all templates in the account from Routee. |
| [Retrieve a list of campaigns created by this book](actions/retrieve-a-list-of-campaigns-created-by-this-book.md) | GET | Retrieves a list of campaigns created by this book from Routee. |
| [Retrieve information for a specific email address from a specific campaign](actions/retrieve-information-for-a-specific-email-address-from-a-specific-campaign.md) | GET | Retrieves information for a specific email address from a specific campaign in Routee. |
| [Retrieve the list of campaigns](actions/retrieve-the-list-of-campaigns.md) | GET | Retrieves the list of campaigns from Routee. |
| [Template creation](actions/template-creation.md) | POST | Creates a new template in Routee. |

### Email Api V1 / Mailing Lists

| Action | Method | Description |
| --- | --- | --- |
| [Add emails to a mailing list](actions/add-emails-to-a-mailing-list.md) | POST | Adds emails to a mailing list in Routee. |
| [Calculate the cost of a campaign carried out by a mailing list](actions/calculate-the-cost-of-a-campaign-carried-out-by-a-mailing-list.md) | GET | Calculates the cost of a campaign carried out by a mailing list in Routee. |
| [Create a mailing list](actions/create-a-mailing-list.md) | POST | Creates a mailing list in Routee. |
| [Delete emails from a mailing list](actions/delete-emails-from-a-mailing-list.md) | DELETE | Deletes emails from a mailing list in Routee. |
| [Edit a mailing list](actions/edit-a-mailing-list.md) | PUT | Updates a mailing list in Routee. |
| [Erase a mailing list](actions/erase-a-mailing-list.md) | DELETE | Deletes a mailing list from Routee. |
| [Find all contacts in mailing list by value of variable](actions/find-all-contacts-in-mailing-list-by-value-of-variable.md) | GET | Finds all contacts in mailing list by value of variable in Routee. |
| [Get a list of variables for a mailing list](actions/get-a-list-of-variables-for-a-mailing-list.md) | GET | Retrieves a list of variables for a mailing list from Routee. |
| [Get total number of contacts in mailing list](actions/get-total-number-of-contacts-in-mailing-list.md) | GET | Retrieves total number of contacts in mailing list from Routee. |
| [Retrieve a list of emails from a mailing list](actions/retrieve-a-list-of-emails-from-a-mailing-list.md) | GET | Retrieves a list of emails from a mailing list in Routee. |
| [Retrieve a list of mailing lists](actions/retrieve-a-list-of-mailing-lists.md) | GET | Retrieves a list of mailing lists from Routee. |
| [Retrieve information for specific email address from a mailing list](actions/retrieve-information-for-specific-email-address-from-a-mailing-list.md) | GET | Retrieves information for specific email address from a mailing list in Routee. |
| [Retrieve mailing list information](actions/retrieve-mailing-list-information.md) | GET | Retrieves mailing list information from Routee. |

### Email Api V1 / Senders

| Action | Method | Description |
| --- | --- | --- |
| [Activate a sender](actions/activate-a-sender.md) | POST | Activates an existing sender in Routee. |
| [Add a sender](actions/add-a-sender.md) | POST | Adds a new sender in Routee. |
| [Delete a sender](actions/delete-a-sender.md) | DELETE | Deletes an existing sender from Routee. |
| [Receive the activation code at the sender’s email address](actions/receive-the-activation-code-at-the-senders-email-address.md) | GET | Sends an activation code to the sender email in Routee. |
| [Retrieve a list of all of the senders](actions/retrieve-a-list-of-all-of-the-senders.md) | GET | Retrieves a list of all of the senders from Routee. |

### Email Api V1 / Smtp

| Action | Method | Description |
| --- | --- | --- |
| [Add a domain](actions/add-a-domain.md) | POST | Adds a new domain in Routee. |
| [Erase from the unsubscribed list](actions/erase-from-the-unsubscribed-list.md) | DELETE | Deletes entries from the unsubscribed list in Routee. |
| [Get total amount of bounces](actions/get-total-amount-of-bounces.md) | GET | Retrieves total amount of bounces from Routee. |
| [New domain verification](actions/new-domain-verification.md) | GET | Creates a new domain verification in Routee. |
| [Retrieve a list of allowed domains](actions/retrieve-a-list-of-allowed-domains.md) | GET | Retrieves a list of allowed domains from Routee. |
| [Retrieve a list of emails](actions/retrieve-a-list-of-emails.md) | GET | Retrieves a list of emails from Routee. |
| [Retrieve bounces per 24 hours](actions/retrieve-bounces-per24-hours.md) | GET | Retrieves bounces per 24 hours from Routee. |
| [Retrieve information for a specific email](actions/retrieve-information-for-a-specific-email.md) | GET | Retrieves information for a specific email from Routee. |
| [Retrieve information for list of emails](actions/retrieve-information-for-list-of-emails.md) | POST | Retrieves information for list of emails from Routee. |
| [Retrieve the list of unsubscribed](actions/retrieve-the-list-of-unsubscribed.md) | GET | Retrieves the list of unsubscribed from Routee. |
| [Retrieve the sender’s IP address](actions/retrieve-the-senders-ip-address.md) | GET | Retrieves the sender's IP address from Routee. |
| [Retrieve total amount of sent emails](actions/retrieve-total-amount-of-sent-emails.md) | GET | Retrieves total amount of sent emails from Routee. |
| [Send an email](actions/send-an-email.md) | POST | Sends an email message with Routee. |
| [Unsubscribing a recipient](actions/unsubscribing-a-recipient.md) | POST | Unsubscribes a recipient from Routee email delivery. |

### Email Api V2

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve a list of domains](actions/retrieve-a-list-of-domains.md) | GET | Retrieves a list of domains from Routee. |
| [Send Transactional Email](actions/send-transactional-email.md) | POST | Sends transactional email messages with Routee. |
| [Send Transactional Email via SendGrid Compatibility Layer](actions/send-transactional-email-via-sendgrid-compatibility-layer.md) | POST | Sends transactional email through Routee's SendGrid compatibility layer. |

### Email Validator

| Action | Method | Description |
| --- | --- | --- |
| [Perform an Email Validator request](actions/perform-an-email-validator-request.md) | POST | Creates an email validator request in Routee. |
| [Track an Email Validator request](actions/track-an-email-validator-request.md) | GET | Tracks an email validator request in Routee. |
| [Track multiple Email Validator requests with filters based on specific time range](actions/track-multiple-email-validator-requests-with-filters-based-on-specific-time-range.md) | GET | Tracks multiple email validator requests with filters based on specific time range in Routee. |

### Failover

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Failover trackings](actions/retrieve-failover-trackings.md) | GET | Retrieves failover tracking records from Routee. |
| [Search failover trackings](actions/search-failover-trackings.md) | GET | Searches Routee for failover tracking records. |
| [Send a Failover Message](actions/send-a-failover-message.md) | POST | Sends a failover message with Routee. |

### Ip Whitelisting

| Action | Method | Description |
| --- | --- | --- |
| [Delete all IP whitelisting settings for API](actions/delete-all-ip-whitelisting-settings-for-api.md) | DELETE | Deletes all API IP whitelisting settings from Routee. |
| [Get whitelisted IP's for an application](actions/get-whitelisted-ips-for-an-application.md) | GET | Retrieves whitelisted IPs for an application from Routee. |
| [IP whitelisting set up](actions/ip-whitelisting-set-up.md) | PUT | Sets up API IP whitelisting in Routee. |
| [Update the IP whitelisting of API](actions/update-the-ip-whitelisting-of-api.md) | PUT | Updates API IP whitelisting in Routee. |

### Number Lookup

| Action | Method | Description |
| --- | --- | --- |
| [Perform a Lookup enquiry for a mobile number](actions/perform-a-lookup-enquiry-for-a-mobile-number.md) | POST | Creates a number lookup request in Routee. |
| [Track a Number Lookup request](actions/track-a-number-lookup-request.md) | GET | Tracks a number lookup request in Routee. |
| [Track multiple Number Lookup requests with filters](actions/track-multiple-number-lookup-requests-with-filters.md) | GET | Tracks multiple number lookup requests with filters in Routee. |

### Number Validation

| Action | Method | Description |
| --- | --- | --- |
| [Validate a phone number](actions/validate-a-phone-number.md) | GET | Validates a phone number in Routee. |

### Numbers

| Action | Method | Description |
| --- | --- | --- |
| [Cancel a Number](actions/cancel-a-number.md) | DELETE | Cancels an existing number in Routee. |
| [Rent a Number](actions/rent-a-number.md) | POST | Rents a new number in Routee. |
| [Update a Number](actions/update-a-number.md) | PUT | Updates an existing number in Routee. |
| [View all the available numbers](actions/view-all-the-available-numbers.md) | GET | Retrieves all the available numbers from Routee. |
| [View all the available numbers with filters](actions/view-all-the-available-numbers-with-filters.md) | GET | Retrieves all the available numbers with filters from Routee. |
| [View all your numbers](actions/view-all-your-numbers.md) | GET | Retrieves all your numbers from Routee. |

### Pools Api

| Action | Method | Description |
| --- | --- | --- |
| [Add a Number to a pool](actions/add-a-number-to-a-pool.md) | PUT | Adds a number to a pool in Routee. |
| [Create a Pool](actions/create-a-pool.md) | POST | Creates a new pool in Routee. |
| [Delete a number from a pool](actions/delete-a-number-from-a-pool.md) | DELETE | Removes a number from a pool in Routee. |
| [Delete a Pool](actions/delete-a-pool.md) | DELETE | Deletes an existing pool from Routee. |
| [Edit a Pool](actions/edit-a-pool.md) | PUT | Updates an existing pool in Routee. |
| [Retrieve all the Pools of an account](actions/retrieve-all-the-pools-of-an-account.md) | GET | Retrieves all the pools of an account from Routee. |
| [Retrieve info for a specific Pool](actions/retrieve-info-for-a-specific-pool.md) | GET | Retrieves info for a specific pool from Routee. |
| [Retrieve the Numbers that belongs to a specific Pool](actions/retrieve-the-numbers-that-belongs-to-a-specific-pool.md) | GET | Retrieves the numbers that belongs to a specific pool from Routee. |
| [Send SMS using a Pool](actions/send-sms-using-a-pool.md) | POST | Sends SMS using a pool with Routee. |

### Push Notifications

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve the details of a Push Notification](actions/retrieve-the-details-of-a-push-notification.md) | GET | Retrieves the details of a push notification from Routee. |
| [Send a Single Push Notification](actions/send-a-single-push-notification.md) | POST | Sends a single push notification with Routee. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Check Account Balance](actions/check-account-balance.md) | GET | Retrieves your current Routee account balance. |

### Statistic Reports

| Action | Method | Description |
| --- | --- | --- |
| [View Time Summary Analytics for a bulk send out - campaign](actions/view-time-summary-analytics-for-a-bulk-send-out-campaign.md) | GET | Retrieves time summary analytics for a bulk send out - campaign from Routee. |
| [View Time Summary Analytics for a country](actions/view-time-summary-analytics-for-a-country.md) | GET | Retrieves time summary analytics for a country from Routee. |
| [View Time Summary Analytics for a country and a network](actions/view-time-summary-analytics-for-a-country-and-a-network.md) | GET | Retrieves time summary analytics for a country and a network from Routee. |
| [View Time Summary Analytics for a range of Messages](actions/view-time-summary-analytics-for-a-range-of-messages.md) | GET | Retrieves time summary analytics for a range of messages from Routee. |
| [View Volume and Price Analytics for a range of Lookup Records](actions/view-volume-and-price-analytics-for-a-range-of-lookup-records.md) | GET | Retrieves volume and price analytics for a range of lookup records from Routee. |
| [View Volume and Price Analytics for a range of Messages](actions/view-volume-and-price-analytics-for-a-range-of-messages.md) | GET | Retrieves volume and price analytics for a range of messages from Routee. |
| [View Volume and Price Analytics for a range of Number Validator Records](actions/view-volume-and-price-analytics-for-a-range-of-number-validator-records.md) | GET | Retrieves volume and price analytics for a range of number validator records from Routee. |
| [View Volume and Price Analytics for a specific bulk send out - campaign](actions/view-volume-and-price-analytics-for-a-specific-bulk-send-out-campaign.md) | GET | Retrieves volume and price analytics for a specific bulk send out - campaign from Routee. |
| [View Volume and Price Analytics for a specific country](actions/view-volume-and-price-analytics-for-a-specific-country.md) | GET | Retrieves volume and price analytics for a specific country from Routee. |
| [View Volume and Price Analytics for a specific country and Network](actions/view-volume-and-price-analytics-for-a-specific-country-and-network.md) | GET | Retrieves volume and price analytics for a specific country and network from Routee. |

### Telegram Api

| Action | Method | Description |
| --- | --- | --- |
| [Check Send Ability](actions/check-send-ability.md) | GET | Retrieves your Routee send ability status. |
| [Check Verification Status](actions/check-verification-status.md) | GET | Retrieves the verification status from Routee. |
| [Revoke Verification Message](actions/revoke-verification-message.md) | DELETE | Revokes a verification message in Routee. |
| [Send Verification Message](actions/send-verification-message.md) | POST | Sends a verification message with Routee. |

### Text Messaging

| Action | Method | Description |
| --- | --- | --- |
| [Analyse an SMS message](actions/analyse-an-sms-message.md) | GET | Analyzes an SMS message in Routee. |
| [Analyze Bulk Messages - Campaigns](actions/analyze-bulk-messages-campaigns.md) | GET | Analyzes bulk message campaigns in Routee. |
| [Delete a scheduled bulk send out - campaign](actions/delete-a-scheduled-bulk-send-out-campaign.md) | DELETE | Deletes a scheduled bulk send out - campaign from Routee. |
| [Retrieve details for a bulk send out - campaign](actions/retrieve-details-for-a-bulk-send-out-campaign.md) | GET | Retrieves details for a bulk send out - campaign from Routee. |
| [Retrieve the countries that are supported by Quiet Hours feature](actions/retrieve-the-countries-that-are-supported-by-quiet-hours-feature.md) | GET | Retrieves the countries that are supported by quiet hours feature from Routee. |
| [Send an SMS](actions/send-an-sms.md) | POST | Sends an SMS message with Routee. |
| [Send Bulk Messages - Campaigns](actions/send-bulk-messages-campaigns.md) | POST | Sends bulk messages - campaigns with Routee. |
| [Track an SMS](actions/track-an-sms.md) | GET | Tracks an SMS message in Routee. |
| [Track multiple messages for a specific bulk send out - campaign](actions/track-multiple-messages-for-a-specific-bulk-send-out-campaign.md) | GET | Tracks multiple messages for a specific bulk send out - campaign in Routee. |
| [Track multiple messages with filters for a specific time range](actions/track-multiple-messages-with-filters-for-a-specific-time-range.md) | GET | Tracks multiple messages with filters for a specific time range in Routee. |
| [Update a scheduled bulk send out - campaign](actions/update-a-scheduled-bulk-send-out-campaign.md) | PUT | Updates a scheduled bulk send out - campaign in Routee. |

### Two Factor Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Cancel a pending verification](actions/cancel-a-pending-verification.md) | DELETE | Cancels a pending verification in Routee. |
| [Confirm a verification by its ID](actions/confirm-a-verification-by-its-id.md) | PUT | Confirms a verification by its ID in Routee. |
| [Get Statistic Reports for all your account verifications](actions/get-statistic-reports-for-all-your-account-verifications.md) | GET | Retrieves statistic reports for all your account verifications from Routee. |
| [Perform a verification](actions/perform-a-verification.md) | POST | Creates a new verification in Routee. |
| [Retrieve a verification status](actions/retrieve-a-verification-status.md) | GET | Retrieves a verification status from Routee. |
| [Retrieve Verification Statistics for any of your account applications](actions/retrieve-verification-statistics-for-any-of-your-account-applications.md) | GET | Retrieves verification statistics for any of your account applications from Routee. |

### Url Services

| Action | Method | Description |
| --- | --- | --- |
| [Perform a URL analysis](actions/perform-a-url-analysis.md) | POST | Analyzes a URL request in Routee. |

### Url Shortener

| Action | Method | Description |
| --- | --- | --- |
| [Get a list of available domains](actions/get-a-list-of-available-domains.md) | GET | Retrieves a list of available domains from Routee. |
| [Get paged analytics](actions/get-paged-analytics.md) | GET | Retrieves paged analytics data from Routee. |
| [Get shorten URL info for monitoring purposes](actions/get-shorten-url-info-for-monitoring-purposes.md) | GET | Retrieves shortened URL monitoring details from Routee. |
| [URL shortener](actions/url-shortener.md) | POST | Creates a shortened URL in Routee. |

### Viber

| Action | Method | Description |
| --- | --- | --- |
| [Delete a scheduled Viber campaign](actions/delete-a-scheduled-viber-campaign.md) | DELETE | Deletes a scheduled Viber campaign from Routee. |
| [Get all Viber Session Messages by a Phone Number](actions/get-all-viber-session-messages-by-a-phone-number.md) | GET | Retrieves all Viber session messages by a phone number from Routee. |
| [Get Viber Session Messages by a Session Id](actions/get-viber-session-messages-by-a-session-id.md) | GET | Retrieves Viber session messages by a session id from Routee. |
| [Retrieve Viber Single Message by Tracking Id](actions/retrieve-viber-single-message-by-tracking-id.md) | GET | Retrieves Viber single message by tracking id from Routee. |
| [Retrieve Viber Trackings by Campaign](actions/retrieve-viber-trackings-by-campaign.md) | GET | Retrieves Viber trackings by campaign from Routee. |
| [Send a Viber Campaign](actions/send-a-viber-campaign.md) | POST | Sends a Viber campaign with Routee. |
| [Send a Viber Single Message](actions/send-a-viber-single-message.md) | POST | Sends a Viber single message with Routee. |
| [Send a Viber Verification Message (OTP)](actions/send-a-viber-verification-message-otp.md) | POST | Sends a Viber verification message (OTP) with Routee. |

### Voice Call Handling

| Action | Method | Description |
| --- | --- | --- |
| [Hangup/reject an active call](actions/hangupreject-an-active-call.md) | PUT | Hangs up or rejects an active call in Routee. |
| [Send DTMF tones to an active call](actions/send-dtmf-tones-to-an-active-call.md) | POST | Sends DTMF tones to an active call with Routee. |
| [Start playing a text-to-speech message to an active call](actions/start-playing-a-text-to-speech-message-to-an-active-call.md) | PUT | Starts playing a text-to-speech message to an active call in Routee. |
| [Start playing an audio file to an active call](actions/start-playing-an-audio-file-to-an-active-call.md) | PUT | Starts playing an audio file to an active call in Routee. |
| [Start recording an active call](actions/start-recording-an-active-call.md) | PUT | Starts recording an active call in Routee. |
| [Stop playing a text-to-speech message to an active call](actions/stop-playing-a-text-to-speech-message-to-an-active-call.md) | DELETE | Stops playing a text-to-speech message to an active call in Routee. |
| [Stop playing an audio file to an active call](actions/stop-playing-an-audio-file-to-an-active-call.md) | DELETE | Stops playing an audio file to an active call in Routee. |
| [Stop recording an active call](actions/stop-recording-an-active-call.md) | DELETE | Stops recording an active call in Routee. |
| [Transfer an active call](actions/transfer-an-active-call.md) | PUT | Transfers an active call in Routee. |

### Voice Conversation

| Action | Method | Description |
| --- | --- | --- |
| [Perform a voice conversation](actions/perform-a-voice-conversation.md) | POST | Creates a voice conversation in Routee. |
| [Retrieve a Conversation Recording](actions/retrieve-a-conversation-recording.md) | GET | Retrieves a conversation recording from Routee. |
| [Retrieve Conversation by TrackingId](actions/retrieve-conversation-by-trackingid.md) | GET | Retrieves conversation by tracking ID from Routee. |
| [Retrieve Conversation dial Tracking](actions/retrieve-conversation-dial-tracking.md) | GET | Retrieves conversation dial tracking from Routee. |

### Voice Messaging

| Action | Method | Description |
| --- | --- | --- |
| [Analyze a Voice Campaign](actions/analyze-a-voice-campaign.md) | GET | Analyzes a voice campaign in Routee. |
| [Delete a scheduled Voice campaign](actions/delete-a-scheduled-voice-campaign.md) | DELETE | Deletes a scheduled voice campaign from Routee. |
| [Retrieve Voice Message Tracking](actions/retrieve-voice-message-tracking.md) | GET | Retrieves voice message tracking from Routee. |
| [Retrieve Voice Trackings by Campaign](actions/retrieve-voice-trackings-by-campaign.md) | GET | Retrieves voice trackings by campaign from Routee. |
| [Send a Voice Campaign](actions/send-a-voice-campaign.md) | POST | Sends a voice campaign with Routee. |
| [Track multiple voice messages with filters for a specific time range](actions/track-multiple-voice-messages-with-filters-for-a-specific-time-range.md) | GET | Tracks multiple voice messages with filters for a specific time range in Routee. |

### Waymore Api

| Action | Method | Description |
| --- | --- | --- |
| [Events data API](actions/events-data-api.md) | POST | Retrieves event data records from Routee. |
| [Mass API](actions/mass-api.md) | POST | Creates a mass data request in Routee. |

### Whatsapp

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Whatsapp Campaign history](actions/retrieve-whatsapp-campaign-history.md) | GET | Retrieves WhatsApp campaign history from Routee. |
| [Retrieve Whatsapp Campaign info](actions/retrieve-whatsapp-campaign-info.md) | GET | Retrieves WhatsApp campaign info from Routee. |
| [Retrieve Whatsapp template status](actions/retrieve-whatsapp-template-status.md) | GET | Retrieves WhatsApp template status from Routee. |
| [Send a Whatsapp campaign](actions/send-a-whatsapp-campaign.md) | POST | Sends a WhatsApp campaign with Routee. |
| [Setup Webhook](actions/setup-webhook.md) | PUT | Sets up a webhook in Routee. |
| [Submit Whatsapp Template for review](actions/submit-whatsapp-template-for-review.md) | POST | Submits a WhatsApp template for review in Routee. |

