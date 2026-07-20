# Routee: Native API Reference

A consolidated summary of Routee's API configuration and 188 documented operations, with links to official documentation.

- **Official docs:** https://docs.routee.net/
- **API base URL:** `https://connect.routee.net`

## Authentication

### OAuth 2.0

Routee uses OAuth 2.0 client credentials with a Routee Application ID and Application Secret.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to https://auth.routee.net/oauth/token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


A machine-to-machine flow is configured.

[Official authentication documentation](https://docs.routee.net/reference/authentication)

## Endpoints (188 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate a sender](actions/activate-a-sender.md) | `POST /senders/:email/code` | [docs](https://docs.routee.net/reference/activating-a-sender) |
| [Add a domain](actions/add-a-domain.md) | `POST /smtp/domains` | [docs](https://docs.routee.net/reference/adding-a-domain) |
| [Add a Number to a pool](actions/add-a-number-to-a-pool.md) | `PUT /pools/my/:poolId/numbers/:msisdn` | [docs](https://docs.routee.net/reference/add-a-number-to-a-pool) |
| [Add a sender](actions/add-a-sender.md) | `POST /senders` | [docs](https://docs.routee.net/reference/adding-a-sender) |
| [Add Contacts to a specified group](actions/add-contacts-to-a-specified-group.md) | `POST /groups/my/:name/contacts` | [docs](https://docs.routee.net/reference/add-contacts-to-a-specified-group) |
| [Add contacts to blacklist](actions/add-contacts-to-blacklist.md) | `POST /contacts/my/blacklist/:service` | [docs](https://docs.routee.net/reference/add-contacts-to-blacklist) |
| [Add emails to a mailing list](actions/add-emails-to-a-mailing-list.md) | `POST /addressbooks/:id/emails` | [docs](https://docs.routee.net/reference/adding-emails-to-a-mailing-list) |
| [Analyse an SMS message](actions/analyse-an-sms-message.md) | `POST /sms/analyze` | [docs](https://docs.routee.net/reference/smsanalyze) |
| [Analyze a Voice Campaign](actions/analyze-a-voice-campaign.md) | `POST /voice/analysis` | [docs](https://docs.routee.net/reference/analyze-a-voice-campaign) |
| [Analyze Bulk Messages - Campaigns](actions/analyze-bulk-messages-campaigns.md) | `POST /sms/analyze/campaign` | [docs](https://docs.routee.net/reference/analyze-bulk-messages) |
| [Blacklisting an email address](actions/blacklisting-an-email-address.md) | `POST /blacklist` | [docs](https://docs.routee.net/reference/blacklisting-an-email-address) |
| [Calculate the cost of a campaign carried out by a mailing list](actions/calculate-the-cost-of-a-campaign-carried-out-by-a-mailing-list.md) | `GET /addressbooks/:id/cost` | [docs](https://docs.routee.net/reference/calculating-the-cost-of-a-campaign-carried-out-by-a-mailing-list) |
| [Campaign information](actions/campaign-information.md) | `GET /campaigns/:id` | [docs](https://docs.routee.net/reference/campaign-information) |
| [Cancel a campaign](actions/cancel-a-campaign.md) | `DELETE /campaigns/:id` | [docs](https://docs.routee.net/reference/cancelling-a-campaign) |
| [Cancel a Number](actions/cancel-a-number.md) | `DELETE /numbers/my/:msisdn` | [docs](https://docs.routee.net/reference/cancel-a-number) |
| [Cancel a pending verification](actions/cancel-a-pending-verification.md) | `DELETE /2step/:trackingId` | [docs](https://docs.routee.net/reference/cancel-verification) |
| [Change Variable for an Email Contact](actions/change-variable-for-an-email-contact.md) | `POST /addressbooks/:addressBookId/emails/variable` | [docs](https://docs.routee.net/reference/testinput-1) |
| [Check Account Balance](actions/check-account-balance.md) | `GET /accounts/me/balance` | [docs](https://docs.routee.net/reference/check-your-account-balance) |
| [Check Send Ability](actions/check-send-ability.md) | `POST /telegram/checkSendAbility` | [docs](https://docs.routee.net/reference/check-send-ability) |
| [Check the user’s balance](actions/check-the-users-balance.md) | `GET /balance` | [docs](https://docs.routee.net/reference/checking-the-users-balance) |
| [Check Verification Status](actions/check-verification-status.md) | `POST /telegram/checkVerificationStatus` | [docs](https://docs.routee.net/reference/check-verification-status) |
| [Confirm a verification by its ID](actions/confirm-a-verification-by-its-id.md) | `POST /2step/:trackingId` | [docs](https://docs.routee.net/reference/confirm-verification) |
| [Country statistics](actions/country-statistics.md) | `GET /campaigns/:id/countries` | [docs](https://docs.routee.net/reference/country-statistics) |
| [Create a campaign](actions/create-a-campaign.md) | `POST /campaigns` | [docs](https://docs.routee.net/reference/creating-a-campaign) |
| [Create a mailing list](actions/create-a-mailing-list.md) | `POST /addressbooks` | [docs](https://docs.routee.net/reference/creating-a-mailing-list) |
| [Create a new contact](actions/create-a-new-contact.md) | `POST /contacts/my` | [docs](https://docs.routee.net/reference/create-a-new-contact) |
| [Create a new group](actions/create-a-new-group.md) | `POST /groups/my` | [docs](https://docs.routee.net/reference/create-a-new-group) |
| [Create a Pool](actions/create-a-pool.md) | `POST /pools/my` | [docs](https://docs.routee.net/reference/create-a-pool) |
| [Create group from difference](actions/create-group-from-difference.md) | `POST /groups/my/difference` | [docs](https://docs.routee.net/reference/create-group-from-difference) |
| [Create Labels](actions/create-labels.md) | `POST /contacts/labels/my` | [docs](https://docs.routee.net/reference/create-labels) |
| [Delete a contact](actions/delete-a-contact.md) | `DELETE /contacts/my/:id` | [docs](https://docs.routee.net/reference/delete-a-contact) |
| [Delete a number from a pool](actions/delete-a-number-from-a-pool.md) | `DELETE /pools/my/:poolId/numbers/:msisdn` | [docs](https://docs.routee.net/reference/delete-a-number-from-a-pool) |
| [Delete a Pool](actions/delete-a-pool.md) | `DELETE /pools/my/:poolId` | [docs](https://docs.routee.net/reference/delete-a-pool) |
| [Delete a scheduled bulk send out - campaign](actions/delete-a-scheduled-bulk-send-out-campaign.md) | `DELETE /sms/:trackingId` | [docs](https://docs.routee.net/reference/delete-a-scheduled-campaign) |
| [Delete a scheduled Viber campaign](actions/delete-a-scheduled-viber-campaign.md) | `DELETE /viber/campaign/:campaignTrackingId` | [docs](https://docs.routee.net/reference/delete-a-scheduled-viber-campaign) |
| [Delete a scheduled Voice campaign](actions/delete-a-scheduled-voice-campaign.md) | `DELETE /voice/campaign/:trackingId` | [docs](https://docs.routee.net/reference/delete-a-voice-campaign) |
| [Delete a sender](actions/delete-a-sender.md) | `DELETE /senders` | [docs](https://docs.routee.net/reference/deleting-a-sender) |
| [Delete all IP whitelisting settings for API](actions/delete-all-ip-whitelisting-settings-for-api.md) | `DELETE /security/whitelist` | [docs](https://docs.routee.net/reference/delete-all-ip-whitelisting-settings-for-api) |
| [Delete emails from a mailing list](actions/delete-emails-from-a-mailing-list.md) | `DELETE /addressbooks/:listId/emails` | [docs](https://docs.routee.net/reference/deleting-emails-from-a-mailing-list) |
| [Delete Groups](actions/delete-groups.md) | `DELETE /groups/my` | [docs](https://docs.routee.net/reference/delete-groups) |
| [Delete multiple contacts](actions/delete-multiple-contacts.md) | `DELETE /contacts/my` | [docs](https://docs.routee.net/reference/delete-multiple-contacts) |
| [Detailed balance info](actions/detailed-balance-info.md) | `GET /user/balance/detail` | [docs](https://docs.routee.net/reference/detailed-balance-info) |
| [Edit a mailing list](actions/edit-a-mailing-list.md) | `PUT /addressbooks/:id` | [docs](https://docs.routee.net/reference/editing-a-mailing-list) |
| [Edit a Pool](actions/edit-a-pool.md) | `PUT /pools/my/:poolId` | [docs](https://docs.routee.net/reference/edit-a-pool) |
| [Edit planned campaign](actions/edit-planned-campaign.md) | `PATCH /campaigns` | [docs](https://docs.routee.net/reference/editing-planned-campaign) |
| [Edit template](actions/edit-template.md) | `POST /template/edit/:id` | [docs](https://docs.routee.net/reference/edit-template) |
| [Erase a mailing list](actions/erase-a-mailing-list.md) | `DELETE /addressbooks/:id` | [docs](https://docs.routee.net/reference/erasing-a-mailing-list) |
| [Erase an email address from all mailing lists](actions/erase-an-email-address-from-all-mailing-lists.md) | `DELETE /emails/:email` | [docs](https://docs.routee.net/reference/erasing-an-email-address-from-all-mailing-lists) |
| [Erase an email address from the blacklist](actions/erase-an-email-address-from-the-blacklist.md) | `DELETE /blacklist` | [docs](https://docs.routee.net/reference/erasing-an-email-address-from-the-blacklist) |
| [Erase from the unsubscribed list](actions/erase-from-the-unsubscribed-list.md) | `DELETE /smtp/unsubscribe` | [docs](https://docs.routee.net/reference/erasing-from-the-unsubscribed-list) |
| [Events data API](actions/events-data-api.md) | `POST /event` | [docs](https://docs.routee.net/reference/events-data-api) |
| [Find all contacts in mailing list by value of variable](actions/find-all-contacts-in-mailing-list-by-value-of-variable.md) | `GET /addressbooks/:id/variables/:variableName/:searchValue` | [docs](https://docs.routee.net/reference/find-all-contacts-in-mailing-list-by-value-of-variable) |
| [Get a list of available domains](actions/get-a-list-of-available-domains.md) | `GET /shorten/domains` | [docs](https://docs.routee.net/reference/get-a-list-of-available-domains) |
| [Get a list of variables for a mailing list](actions/get-a-list-of-variables-for-a-mailing-list.md) | `GET /addressbooks/:id/variables` | [docs](https://docs.routee.net/reference/get-a-list-of-variables-for-a-mailing-list) |
| [Get all Viber Session Messages by a Phone Number](actions/get-all-viber-session-messages-by-a-phone-number.md) | `POST /viber/session` | [docs](https://docs.routee.net/reference/get-all-viber-session-messages-by-a-phone-number) |
| [Get blacklisted contacts for service](actions/get-blacklisted-contacts-for-service.md) | `GET /contacts/my/blacklist/:service` | [docs](https://docs.routee.net/reference/get-blacklisted-contacts-for-service) |
| [Get info about template](actions/get-info-about-template.md) | `GET /template/:templateId` | [docs](https://docs.routee.net/reference/get-info-about-template) |
| [Get paged analytics](actions/get-paged-analytics.md) | `GET /shorten/:trackingId/analytics` | [docs](https://docs.routee.net/reference/getting-paged-analytics) |
| [Get pricing for all Routee Services](actions/get-pricing-for-all-routee-services.md) | `GET /system/prices` | [docs](https://docs.routee.net/reference/pricing) |
| [Get shorten URL info for monitoring purposes](actions/get-shorten-url-info-for-monitoring-purposes.md) | `GET /shorten/:trackingId` | [docs](https://docs.routee.net/reference/getting-shorten-url-info-for-monitoring-purposes) |
| [Get Statistic Reports for all your account verifications](actions/get-statistic-reports-for-all-your-account-verifications.md) | `GET /2step/reports` | [docs](https://docs.routee.net/reference/verification-reports) |
| [Get total amount of bounces](actions/get-total-amount-of-bounces.md) | `GET /smtp/bounces/day/total` | [docs](https://docs.routee.net/reference/get-total-amount-of-bounces) |
| [Get total number of contacts in mailing list](actions/get-total-number-of-contacts-in-mailing-list.md) | `GET /addressbooks/:id/emails/total` | [docs](https://docs.routee.net/reference/get-total-number-of-contacts-in-mailing-list) |
| [Get Viber Session Messages by a Session Id](actions/get-viber-session-messages-by-a-session-id.md) | `GET /viber/session/:sessionId` | [docs](https://docs.routee.net/reference/get-viber-session-by-a-sessionid) |
| [Get whitelisted IP's for an application](actions/get-whitelisted-ips-for-an-application.md) | `GET /security/whitelist` | [docs](https://docs.routee.net/reference/get-whitelisted-ips-for-an-application) |
| [Get your account transactions](actions/get-your-account-transactions.md) | `GET /accounts/me/transactions` | [docs](https://docs.routee.net/reference/transactions) |
| [Hangup/reject an active call](actions/hangupreject-an-active-call.md) | `PUT /voice/conversation/:messageId` | [docs](https://docs.routee.net/reference/hangupreject-an-active-call) |
| [IP whitelisting set up](actions/ip-whitelisting-set-up.md) | `POST /security/whitelist` | [docs](https://docs.routee.net/reference/ip-whitelisting-set-up) |
| [Mass API](actions/mass-api.md) | `POST /data` | [docs](https://docs.routee.net/reference/mass-api) |
| [Merge multiple groups](actions/merge-multiple-groups.md) | `POST /groups/my/merge` | [docs](https://docs.routee.net/reference/merge-multiple-groups) |
| [New domain verification](actions/new-domain-verification.md) | `GET /smtp/domains/:email` | [docs](https://docs.routee.net/reference/new-domain-verification) |
| [Perform a Lookup enquiry for a mobile number](actions/perform-a-lookup-enquiry-for-a-mobile-number.md) | `POST /lookup` | [docs](https://docs.routee.net/reference/perform-a-lookup-validation-for-a-mobile-nummer) |
| [Perform a URL analysis](actions/perform-a-url-analysis.md) | `POST /urlinsights` | [docs](https://docs.routee.net/reference/perform-a-url-analysis) |
| [Perform a verification](actions/perform-a-verification.md) | `POST /2step` | [docs](https://docs.routee.net/reference/verification) |
| [Perform a voice conversation](actions/perform-a-voice-conversation.md) | `POST /voice/conversation` | [docs](https://docs.routee.net/reference/perform-a-voice-conversation) |
| [Perform an Email Validator request](actions/perform-an-email-validator-request.md) | `POST /emailvalidator` | [docs](https://docs.routee.net/reference/perform-an-email-validator-request) |
| [Receive the activation code at the sender’s email address](actions/receive-the-activation-code-at-the-senders-email-address.md) | `GET /senders/:email/code` | [docs](https://docs.routee.net/reference/receiving-the-activation-code-at-the-senders-email-address) |
| [Referrals statistics](actions/referrals-statistics.md) | `GET /campaigns/:id/referrals` | [docs](https://docs.routee.net/reference/referrals-statistics) |
| [Remove a group of contacts from the blacklist](actions/remove-a-group-of-contacts-from-the-blacklist.md) | `DELETE /contacts/my/blacklist/:service/groups` | [docs](https://docs.routee.net/reference/remove-a-group-of-contacts-from-the-blacklist) |
| [Remove Contacts from blacklist](actions/remove-contacts-from-blacklist.md) | `DELETE /contacts/my/blacklist/:service` | [docs](https://docs.routee.net/reference/remove-contacts-from-blacklist) |
| [Remove Contacts of a specified group](actions/remove-contacts-of-a-specified-group.md) | `DELETE /groups/my/:groupName/contacts` | [docs](https://docs.routee.net/reference/remove-contacts-of-a-specified-group) |
| [Rent a Number](actions/rent-a-number.md) | `POST /numbers/my` | [docs](https://docs.routee.net/reference/rent-a-number) |
| [Retrieve a Conversation Recording](actions/retrieve-a-conversation-recording.md) | `GET /recordings/my/downloads/:recordingTrackingId` | [docs](https://docs.routee.net/reference/retrieve-conversation-recording) |
| [Retrieve a list of all of the senders](actions/retrieve-a-list-of-all-of-the-senders.md) | `GET /senders` | [docs](https://docs.routee.net/reference/retrieving-a-list-of-all-of-the-senders) |
| [Retrieve a list of all templates in the account](actions/retrieve-a-list-of-all-templates-in-the-account.md) | `GET /templates` | [docs](https://docs.routee.net/reference/retrieving-a-list-of-all-templates-in-the-account) |
| [Retrieve a list of allowed domains](actions/retrieve-a-list-of-allowed-domains.md) | `GET /smtp/domains` | [docs](https://docs.routee.net/reference/retrieving-a-list-of-allowed-domains) |
| [Retrieve a list of campaigns created by this book](actions/retrieve-a-list-of-campaigns-created-by-this-book.md) | `GET /addressbooks/:id/campaigns` | [docs](https://docs.routee.net/reference/retrieving-a-list-of-campaigns-created-by-this-book) |
| [Retrieve a list of domains](actions/retrieve-a-list-of-domains.md) | `GET /email-senders/domain` | [docs](https://docs.routee.net/reference/email-api-v2-retrieving-a-list-of-domains) |
| [Retrieve a list of emails](actions/retrieve-a-list-of-emails.md) | `GET /smtp/emails` | [docs](https://docs.routee.net/reference/retrieving-a-list-of-emails) |
| [Retrieve a list of emails from a mailing list](actions/retrieve-a-list-of-emails-from-a-mailing-list.md) | `GET /:id/emails` | [docs](https://docs.routee.net/reference/retrieving-a-list-of-emails-from-a-mailing-list) |
| [Retrieve a list of mailing lists](actions/retrieve-a-list-of-mailing-lists.md) | `GET /addressbooks` | [docs](https://docs.routee.net/reference/retrieving-a-list-of-mailing-lists) |
| [Retrieve a verification status](actions/retrieve-a-verification-status.md) | `GET /2step/:trackingId` | [docs](https://docs.routee.net/reference/retrieve-a-verification-status) |
| [Retrieve all the contacts](actions/retrieve-all-the-contacts.md) | `GET /contacts/my` | [docs](https://docs.routee.net/reference/retrieve-all-the-contacts) |
| [Retrieve all the Pools of an account](actions/retrieve-all-the-pools-of-an-account.md) | `GET /pools/my` | [docs](https://docs.routee.net/reference/retrieve-all-the-pools-of-an-account) |
| [Retrieve bounces per 24 hours](actions/retrieve-bounces-per24-hours.md) | `GET /smtp/bounces/day` | [docs](https://docs.routee.net/reference/retrieving-bounces-per-24-hours) |
| [Retrieve Conversation by TrackingId](actions/retrieve-conversation-by-trackingid.md) | `GET /voice/conversation/:conversationTrackingId` | [docs](https://docs.routee.net/reference/retrieve-conversation-tracking) |
| [Retrieve Conversation dial Tracking](actions/retrieve-conversation-dial-tracking.md) | `GET /voice/tracking/conversation/:conversationTrackingId` | [docs](https://docs.routee.net/reference/retrieve-conversation-dial-tracking) |
| [Retrieve detail information about a specific email address](actions/retrieve-detail-information-about-a-specific-email-address.md) | `GET /emails/:email/details` | [docs](https://docs.routee.net/reference/retrieve-detail-information-about-a-specific-email-address) |
| [Retrieve details about a contact](actions/retrieve-details-about-a-contact.md) | `GET /contacts/my/:id` | [docs](https://docs.routee.net/reference/retrieve-details-about-a-contact) |
| [Retrieve details for a bulk send out - campaign](actions/retrieve-details-for-a-bulk-send-out-campaign.md) | `GET /campaigns/:trackingId` | [docs](https://docs.routee.net/reference/retrieve-details-for-a-campaign) |
| [Retrieve Failover trackings](actions/retrieve-failover-trackings.md) | `GET /failover/tracking/:trackingId` | [docs](https://docs.routee.net/reference/retrieve-failover-trackings) |
| [Retrieve general information about bulk of email address](actions/retrieve-general-information-about-bulk-of-email-address.md) | `POST /emails` | [docs](https://docs.routee.net/reference/retrieve-general-information-about-bulk-of-email-address) |
| [Retrieve general information for a specific email address](actions/retrieve-general-information-for-a-specific-email-address.md) | `GET /emails/:email` | [docs](https://docs.routee.net/reference/retrieve-general-information-for-a-specific-email-address) |
| [Retrieve info for a specific Pool](actions/retrieve-info-for-a-specific-pool.md) | `GET /pools/my/:poolId` | [docs](https://docs.routee.net/reference/retrieve-info-for-a-specific-pool) |
| [Retrieve information for a specific email](actions/retrieve-information-for-a-specific-email.md) | `GET /smtp/emails/:id` | [docs](https://docs.routee.net/reference/retrieving-information-for-a-specific-email) |
| [Retrieve information for a specific email address from a specific campaign](actions/retrieve-information-for-a-specific-email-address-from-a-specific-campaign.md) | `GET /campaigns/:id/email/:email` | [docs](https://docs.routee.net/reference/retrieving-information-for-a-specific-email-address-from-a-specific-campaign) |
| [Retrieve information for list of emails](actions/retrieve-information-for-list-of-emails.md) | `POST /smtp/emails/info` | [docs](https://docs.routee.net/reference/retrieving-information-for-list-of-emails) |
| [Retrieve information for specific email address from a mailing list](actions/retrieve-information-for-specific-email-address-from-a-mailing-list.md) | `GET /addressbooks/:id/emails/:email` | [docs](https://docs.routee.net/reference/retrieving-information-for-specific-email-address-from-a-mailing-list) |
| [Retrieve mailing list information](actions/retrieve-mailing-list-information.md) | `GET /addressbooks/:id` | [docs](https://docs.routee.net/reference/retrieving-mailing-list-information) |
| [Retrieve one of the account's groups](actions/retrieve-one-of-the-accounts-groups.md) | `GET /groups/my/:name` | [docs](https://docs.routee.net/reference/retrieve-one-of-the-accounts-groups) |
| [Retrieve statistics for an email address by campaigns](actions/retrieve-statistics-for-an-email-address-by-campaigns.md) | `GET /emails/:email/campaigns` | [docs](https://docs.routee.net/reference/retrieving-statistics-for-an-email-address-by-campaigns) |
| [Retrieve statistics for email addresses by campaigns and presence in lists](actions/retrieve-statistics-for-email-addresses-by-campaigns-and-presence-in-lists.md) | `POST /emails/campaigns` | [docs](https://docs.routee.net/reference/retrieving-statistics-for-email-addresses-by-campaigns-and-presence-in-lists) |
| [Retrieve the account's contact labels](actions/retrieve-the-accounts-contact-labels.md) | `GET /contacts/labels/my` | [docs](https://docs.routee.net/reference/retrieve-the-accounts-contact-labels) |
| [Retrieve the account's groups](actions/retrieve-the-accounts-groups.md) | `GET /groups/my` | [docs](https://docs.routee.net/reference/retrieve-the-accounts-groups) |
| [Retrieve the account's groups in paged format](actions/retrieve-the-accounts-groups-in-paged-format.md) | `GET /groups/my/page` | [docs](https://docs.routee.net/reference/retrieve-the-accounts-groups-in-paged-format) |
| [Retrieve the countries that are supported by Quiet Hours feature](actions/retrieve-the-countries-that-are-supported-by-quiet-hours-feature.md) | `GET /sms/quietHours/countries/:language` | [docs](https://docs.routee.net/reference/retrieve-the-countries-that-are-supported-by-the-quiet-hours-feature) |
| [Retrieve the details of a Push Notification](actions/retrieve-the-details-of-a-push-notification.md) | `GET /push-notifications/messages/:trackingId` | [docs](https://docs.routee.net/reference/retrieve-the-details-of-a-push-notification) |
| [Retrieve the list of campaigns](actions/retrieve-the-list-of-campaigns.md) | `GET /campaigns` | [docs](https://docs.routee.net/reference/retrieving-the-list-of-campaigns) |
| [Retrieve the list of unsubscribed](actions/retrieve-the-list-of-unsubscribed.md) | `GET /smtp/unsubscribe` | [docs](https://docs.routee.net/reference/retrieving-the-list-of-unsubscribed) |
| [Retrieve the Numbers that belongs to a specific Pool](actions/retrieve-the-numbers-that-belongs-to-a-specific-pool.md) | `GET /pools/my/:poolId/numbers` | [docs](https://docs.routee.net/reference/retrieve-the-numbers-that-belongs-to-a-specific-pool) |
| [Retrieve the sender’s IP address](actions/retrieve-the-senders-ip-address.md) | `GET /smtp/ips` | [docs](https://docs.routee.net/reference/retrieving-the-senders-ip-address) |
| [Retrieve total amount of sent emails](actions/retrieve-total-amount-of-sent-emails.md) | `GET /smtp/emails/total` | [docs](https://docs.routee.net/reference/retrieving-total-amount-of-sent-emails) |
| [Retrieve Verification Statistics for any of your account applications](actions/retrieve-verification-statistics-for-any-of-your-account-applications.md) | `GET /2step/reports/applications/:appId` | [docs](https://docs.routee.net/reference/verification-reports-application) |
| [Retrieve Viber Single Message by Tracking Id](actions/retrieve-viber-single-message-by-tracking-id.md) | `GET /viber/tracking/:trackingId` | [docs](https://docs.routee.net/reference/retrieve-single-viber-tracking) |
| [Retrieve Viber Trackings by Campaign](actions/retrieve-viber-trackings-by-campaign.md) | `GET /viber/tracking/campaign/:campaignTrackingId` | [docs](https://docs.routee.net/reference/retrieve-viber-tracking-by-campaign) |
| [Retrieve Voice Message Tracking](actions/retrieve-voice-message-tracking.md) | `GET /voice/tracking/:messageTrackingId` | [docs](https://docs.routee.net/reference/voicemessagetracking) |
| [Retrieve Voice Trackings by Campaign](actions/retrieve-voice-trackings-by-campaign.md) | `GET /voice/tracking/campaign/:campaignTrackingId` | [docs](https://docs.routee.net/reference/retrieve-voice-tracking-by-campaign) |
| [Retrieve Whatsapp Campaign history](actions/retrieve-whatsapp-campaign-history.md) | `GET /tracking/campaign/:campaignTrackingId/history` | [docs](https://docs.routee.net/reference/retrieve-whatsapp-campaign-history) |
| [Retrieve Whatsapp Campaign info](actions/retrieve-whatsapp-campaign-info.md) | `GET /tracking/campaign/:campaignTrackingId` | [docs](https://docs.routee.net/reference/retrieve-whatsapp-campaign-status) |
| [Retrieve Whatsapp template status](actions/retrieve-whatsapp-template-status.md) | `GET /accounts/templates/:templateId` | [docs](https://docs.routee.net/reference/retrieve-whatsapp-template-status) |
| [Revoke Verification Message](actions/revoke-verification-message.md) | `POST /telegram/revokeVerificationMessage` | [docs](https://docs.routee.net/reference/revoke-verification-message) |
| [Search failover trackings](actions/search-failover-trackings.md) | `POST /failover/tracking` | [docs](https://docs.routee.net/reference/track-multiple-failovers-with-filters-for-a-specific-time-range) |
| [Send a Failover Message](actions/send-a-failover-message.md) | `POST /failover` | [docs](https://docs.routee.net/reference/send-a-failover-message) |
| [Send a Single Push Notification](actions/send-a-single-push-notification.md) | `POST /push-notifications/messages` | [docs](https://docs.routee.net/reference/send-a-single-push-notification) |
| [Send a Viber Campaign](actions/send-a-viber-campaign.md) | `POST /viber/campaign` | [docs](https://docs.routee.net/reference/send-a-viber-campaign) |
| [Send a Viber Single Message](actions/send-a-viber-single-message.md) | `POST /viber` | [docs](https://docs.routee.net/reference/send-a-viber-single-message) |
| [Send a Viber Verification Message (OTP)](actions/send-a-viber-verification-message-otp.md) | `POST /viber/otp` | [docs](https://docs.routee.net/reference/viber-otp-request) |
| [Send a Voice Campaign](actions/send-a-voice-campaign.md) | `POST /voice/campaign` | [docs](https://docs.routee.net/reference/send-a-voice-campaign) |
| [Send a Whatsapp campaign](actions/send-a-whatsapp-campaign.md) | `POST /campaign` | [docs](https://docs.routee.net/reference/send-a-whatsapp-campaign) |
| [Send an email](actions/send-an-email.md) | `POST /smtp/emails` | [docs](https://docs.routee.net/reference/sending-an-email) |
| [Send an SMS](actions/send-an-sms.md) | `POST /sms` | [docs](https://docs.routee.net/reference/send-single-sms) |
| [Send Bulk Messages - Campaigns](actions/send-bulk-messages-campaigns.md) | `POST /sms/campaign` | [docs](https://docs.routee.net/reference/send-bulk-messages) |
| [Send DTMF tones to an active call](actions/send-dtmf-tones-to-an-active-call.md) | `POST /voice/conversation/:messageId/dtmf` | [docs](https://docs.routee.net/reference/send-dtmf-tones-to-an-active-call) |
| [Send SMS using a Pool](actions/send-sms-using-a-pool.md) | `POST /pools/my/:poolId/sms` | [docs](https://docs.routee.net/reference/send-sms-using-a-pool) |
| [Send Transactional Email](actions/send-transactional-email.md) | `POST /transactional-email` | [docs](https://docs.routee.net/reference/email-v2-transactional) |
| [Send Transactional Email via SendGrid Compatibility Layer](actions/send-transactional-email-via-sendgrid-compatibility-layer.md) | `POST /transactional-email/sg/` | [docs](https://docs.routee.net/reference/email-v2-sg-compatibility) |
| [Send Verification Message](actions/send-verification-message.md) | `POST /telegram` | [docs](https://docs.routee.net/reference/send-verification-message) |
| [Setup Webhook](actions/setup-webhook.md) | `POST /webhook` | [docs](https://docs.routee.net/reference/setup-webhook) |
| [Start playing a text-to-speech message to an active call](actions/start-playing-a-text-to-speech-message-to-an-active-call.md) | `POST /voice/conversation/:messageId/talk` | [docs](https://docs.routee.net/reference/start-playing-a-text-to-speech-message-to-an-active-call) |
| [Start playing an audio file to an active call](actions/start-playing-an-audio-file-to-an-active-call.md) | `POST /voice/conversation/:messageId/file` | [docs](https://docs.routee.net/reference/start-playing-an-audio-file-to-an-active-call) |
| [Start recording an active call](actions/start-recording-an-active-call.md) | `POST /voice/conversation/:messageId/record` | [docs](https://docs.routee.net/reference/start-recording-an-active-call) |
| [Stop playing a text-to-speech message to an active call](actions/stop-playing-a-text-to-speech-message-to-an-active-call.md) | `DELETE /voice/conversation/:messageId/talk` | [docs](https://docs.routee.net/reference/stop-playing-a-text-to-speech-message-to-an-active-call) |
| [Stop playing an audio file to an active call](actions/stop-playing-an-audio-file-to-an-active-call.md) | `DELETE /voice/conversation/:messageId/file` | [docs](https://docs.routee.net/reference/stop-playing-an-audio-file-to-an-active-call) |
| [Stop recording an active call](actions/stop-recording-an-active-call.md) | `DELETE /voice/conversation/:messageId/record` | [docs](https://docs.routee.net/reference/stop-recording-an-active-call) |
| [Submit Whatsapp Template for review](actions/submit-whatsapp-template-for-review.md) | `POST /accounts/:whatsappAccountId/templates` | [docs](https://docs.routee.net/reference/submit-whatsapp-text-template-for-review) |
| [Template creation](actions/template-creation.md) | `POST /template` | [docs](https://docs.routee.net/reference/template-creation) |
| [Track a Number Lookup request](actions/track-a-number-lookup-request.md) | `GET /lookup/:lookupId` | [docs](https://docs.routee.net/reference/track-a-single-hlr-lookup-record) |
| [Track an Email Validator request](actions/track-an-email-validator-request.md) | `GET /emailvalidator/tracking/:trackingId` | [docs](https://docs.routee.net/reference/track-an-email-validator-request) |
| [Track an SMS](actions/track-an-sms.md) | `GET /sms/tracking/single/:trackingId` | [docs](https://docs.routee.net/reference/smstrackingsingle) |
| [Track multiple Email Validator requests with filters based on specific time range](actions/track-multiple-email-validator-requests-with-filters-based-on-specific-time-range.md) | `POST /emailvalidator/tracking` | [docs](https://docs.routee.net/reference/track-multiple-email-validator-requests) |
| [Track multiple messages for a specific bulk send out - campaign](actions/track-multiple-messages-for-a-specific-bulk-send-out-campaign.md) | `GET /sms/tracking/campaign/:campaignTrackingId` | [docs](https://docs.routee.net/reference/track-multiple-sms-of-a-specific-campaign) |
| [Track multiple messages with filters for a specific time range](actions/track-multiple-messages-with-filters-for-a-specific-time-range.md) | `POST /sms/tracking` | [docs](https://docs.routee.net/reference/track-multiple-sms-with-filters-for-a-specific-time-range) |
| [Track multiple Number Lookup requests with filters](actions/track-multiple-number-lookup-requests-with-filters.md) | `POST /lookup/tracking` | [docs](https://docs.routee.net/reference/track-multiple-hlr-lookup-records-with-filters-for-a-specific-time-range) |
| [Track multiple voice messages with filters for a specific time range](actions/track-multiple-voice-messages-with-filters-for-a-specific-time-range.md) | `POST /voice/tracking` | [docs](https://docs.routee.net/reference/calltracking) |
| [Transfer an active call](actions/transfer-an-active-call.md) | `POST /voice/conversation/:messageId/transfer` | [docs](https://docs.routee.net/reference/transfer-an-active-call) |
| [Unsubscribe contact from the defined mailing list](actions/unsubscribe-contact-from-the-defined-mailing-list.md) | `GET /addressbooks/:id/emails/unsubscribe` | [docs](https://docs.routee.net/reference/unsubscribe-contact-from-the-defined-mailing-list) |
| [Unsubscribing a recipient](actions/unsubscribing-a-recipient.md) | `POST /smtp/unsubscribe` | [docs](https://docs.routee.net/reference/unsubscribing-a-recipient) |
| [Update a contact's details](actions/update-a-contacts-details.md) | `PUT /contacts/my/:id` | [docs](https://docs.routee.net/reference/update-a-contacts-details) |
| [Update a Number](actions/update-a-number.md) | `PUT /numbers/my/:msisdn` | [docs](https://docs.routee.net/reference/update-a-number) |
| [Update a scheduled bulk send out - campaign](actions/update-a-scheduled-bulk-send-out-campaign.md) | `PUT /sms/:trackingId` | [docs](https://docs.routee.net/reference/update-a-scheduled-message-campaign) |
| [Update the IP whitelisting of API](actions/update-the-ip-whitelisting-of-api.md) | `PATCH /security/whitelist` | [docs](https://docs.routee.net/reference/update-the-ip-whitelisting-of-api) |
| [URL shortener](actions/url-shortener.md) | `POST /shorten/urls` | [docs](https://docs.routee.net/reference/url-shortener) |
| [Validate a phone number](actions/validate-a-phone-number.md) | `POST /numbervalidator` | [docs](https://docs.routee.net/reference/validate) |
| [View all the available numbers](actions/view-all-the-available-numbers.md) | `GET /numbers/available` | [docs](https://docs.routee.net/reference/view-all-the-available-numbers) |
| [View all the available numbers with filters](actions/view-all-the-available-numbers-with-filters.md) | `POST /numbers/available/search` | [docs](https://docs.routee.net/reference/view-all-the-available-numbers-with-filters) |
| [View all your numbers](actions/view-all-your-numbers.md) | `GET /numbers/my` | [docs](https://docs.routee.net/reference/view-all-the-numbers) |
| [View the blacklist](actions/view-the-blacklist.md) | `GET /blacklist` | [docs](https://docs.routee.net/reference/viewing-the-blacklist) |
| [View the Contacts of a specified group](actions/view-the-contacts-of-a-specified-group.md) | `GET /groups/my/:name/contacts` | [docs](https://docs.routee.net/reference/view-the-contacts-of-a-specified-group) |
| [View Time Summary Analytics for a bulk send out - campaign](actions/view-time-summary-analytics-for-a-bulk-send-out-campaign.md) | `GET /reports/my/breakdown/perCampaign` | [docs](https://docs.routee.net/reference/view-time-summary-analytics-for-a-bulk-send-out) |
| [View Time Summary Analytics for a country](actions/view-time-summary-analytics-for-a-country.md) | `GET /reports/my/breakdown/perCountry` | [docs](https://docs.routee.net/reference/view-time-summary-analytics-for-a-country) |
| [View Time Summary Analytics for a country and a network](actions/view-time-summary-analytics-for-a-country-and-a-network.md) | `GET /reports/my/breakdown/perMccMnc` | [docs](https://docs.routee.net/reference/view-time-summary-analytics-for-a-country-and-a-network) |
| [View Time Summary Analytics for a range of Messages](actions/view-time-summary-analytics-for-a-range-of-messages.md) | `GET /reports/my/breakdown` | [docs](https://docs.routee.net/reference/view-time-summary-analytics-for-a-range-of-messages) |
| [View Volume and Price Analytics for a range of Lookup Records](actions/view-volume-and-price-analytics-for-a-range-of-lookup-records.md) | `GET /reports/my/lookup/volPrice` | [docs](https://docs.routee.net/reference/view-volume-and-price-analytics-for-a-range-of-lookup-records) |
| [View Volume and Price Analytics for a range of Messages](actions/view-volume-and-price-analytics-for-a-range-of-messages.md) | `GET /reports/my/volPrice` | [docs](https://docs.routee.net/reference/view-volumeprice-summary-analytics-for-a-range-of-messages) |
| [View Volume and Price Analytics for a range of Number Validator Records](actions/view-volume-and-price-analytics-for-a-range-of-number-validator-records.md) | `GET /reports/my/numberValidator/volPrice` | [docs](https://docs.routee.net/reference/view-number-validator-volume-and-costs-for-a-specified-date-range) |
| [View Volume and Price Analytics for a specific bulk send out - campaign](actions/view-volume-and-price-analytics-for-a-specific-bulk-send-out-campaign.md) | `GET /reports/my/volPrice/perCampaign` | [docs](https://docs.routee.net/reference/view-volume-and-price-analytics-for-a-specific-campaign) |
| [View Volume and Price Analytics for a specific country](actions/view-volume-and-price-analytics-for-a-specific-country.md) | `GET /reports/my/volPrice/perMcc` | [docs](https://docs.routee.net/reference/view-volumeprice-summary-analytics-for-a-country) |
| [View Volume and Price Analytics for a specific country and Network](actions/view-volume-and-price-analytics-for-a-specific-country-and-network.md) | `GET /reports/my/volPrice/perMccMnc` | [docs](https://docs.routee.net/reference/view-volume-and-price-analytics-for-a-specific-country) |
