# Brevo: Native API Reference

A consolidated summary of Brevo's API configuration and 285 documented operations, with links to official documentation.

- **Official docs:** https://developers.brevo.com/docs
- **API base URL:** `https://api.brevo.com`

## Authentication

### API Key Header

Use a Brevo API v3 key sent in the api-key request header.

Send these headers with each API request:

```http
api-key: <apiKey>
```

[Official authentication documentation](https://developers.brevo.com/docs/api-key-authentication)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–2500). Use `offset` in the query string as the record offset; numbering starts at 0.

## Endpoints (285 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Ecommerce](actions/activate-ecommerce.md) | `POST /v3/ecommerce/activate` | [docs](https://developers.brevo.com/reference/activate-the-ecommerce-app) |
| [Add Contacts to List](actions/add-contacts-to-list.md) | `POST /v3/contacts/lists/:listId/contacts/add` | [docs](https://developers.brevo.com/reference/add-contact-to-list) |
| [Assign Loyalty Tier](actions/assign-loyalty-tier.md) | `POST /v3/loyalty/tier/programs/:pid/contacts/:cid/tiers/:tid` | [docs](https://developers.brevo.com/reference/addsubscriptiontotier) |
| [Associate Corporate Sub Account IP](actions/associate-corporate-sub-account-ip.md) | `POST /v3/corporate/subAccount/ip/associate` | [docs](https://developers.brevo.com/reference/associate-an-ip-to-sub-accounts) |
| [Authenticate Sender Domain](actions/authenticate-sender-domain.md) | `PUT /v3/senders/domains/:domainName/authenticate` | [docs](https://developers.brevo.com/reference/authenticatedomain) |
| [Cancel Loyalty Transaction](actions/cancel-loyalty-transaction.md) | `POST /v3/loyalty/balance/programs/:pid/transactions/:tid/cancel` | [docs](https://developers.brevo.com/reference/canceltransaction) |
| [Complete Loyalty Redeem Transaction](actions/complete-loyalty-redeem-transaction.md) | `POST /v3/loyalty/offer/programs/:pid/rewards/redeem/:tid/complete` | [docs](https://developers.brevo.com/reference/completeredeemtransaction) |
| [Complete Loyalty Transaction](actions/complete-loyalty-transaction.md) | `POST /v3/loyalty/balance/programs/:pid/transactions/:tid/complete` | [docs](https://developers.brevo.com/reference/completetransaction) |
| [Create Blocked Domain](actions/create-blocked-domain.md) | `POST /v3/smtp/blockedDomains` | [docs](https://developers.brevo.com/reference/blocknewdomain) |
| [Create Categories Batch](actions/create-categories-batch.md) | `POST /v3/categories/batch` | [docs](https://developers.brevo.com/reference/createupdatebatchcategory) |
| [Create Category](actions/create-category.md) | `POST /v3/categories` | [docs](https://developers.brevo.com/reference/createupdatecategory) |
| [Create Company](actions/create-company.md) | `POST /v3/companies` | [docs](https://developers.brevo.com/reference/createacompany) |
| [Create Contact](actions/create-contact.md) | `POST /v3/contacts` | [docs](https://developers.brevo.com/reference/create-contact) |
| [Create Contact Attribute](actions/create-contact-attribute.md) | `POST /v3/contacts/attributes/:attributeCategory/:attributeName` | [docs](https://developers.brevo.com/reference/create-attribute) |
| [Create Contact Folder](actions/create-contact-folder.md) | `POST /v3/contacts/folders` | [docs](https://developers.brevo.com/reference/createfolder) |
| [Create Contacts Batch](actions/create-contacts-batch.md) | `POST /v3/contacts/batch` | [docs](https://developers.brevo.com/reference/createbatchcontacts) |
| [Create Conversation Message](actions/create-conversation-message.md) | `POST /v3/conversations/messages` | [docs](https://developers.brevo.com/reference/sendamessageasagent) |
| [Create Corporate Group](actions/create-corporate-group.md) | `POST /v3/corporate/group` | [docs](https://developers.brevo.com/reference/create-a-new-group-of-sub-accounts) |
| [Create Corporate SSO Token](actions/create-corporate-sso-token.md) | `POST /v3/corporate/ssoToken` | [docs](https://developers.brevo.com/reference/generate-sso-token-to-access-admin-account) |
| [Create Corporate Sub Account](actions/create-corporate-sub-account.md) | `POST /v3/corporate/subAccount` | [docs](https://developers.brevo.com/reference/create-a-new-sub-account-under-a-master-account) |
| [Create Corporate Sub Account API Key](actions/create-corporate-sub-account-api-key.md) | `POST /v3/corporate/subAccount/key` | [docs](https://developers.brevo.com/reference/create-an-api-key-for-a-sub-account) |
| [Create Corporate Sub Account SSO Token](actions/create-corporate-sub-account-sso-token.md) | `POST /v3/corporate/subAccount/ssoToken` | [docs](https://developers.brevo.com/reference/generate-sso-token-to-access-sub-account) |
| [Create Coupon Collection](actions/create-coupon-collection.md) | `POST /v3/couponCollections` | [docs](https://developers.brevo.com/reference/createcouponcollection) |
| [Create Coupons](actions/create-coupons.md) | `POST /v3/coupons` | [docs](https://developers.brevo.com/reference/createcoupons) |
| [Create CRM Attribute](actions/create-crm-attribute.md) | `POST /v3/crm/attributes` | [docs](https://developers.brevo.com/reference/create-a-company-deal-attribute) |
| [Create CRM File](actions/create-crm-file.md) | `POST /v3/crm/files` | [docs](https://developers.brevo.com/reference/uploadafile) |
| [Create CRM Note](actions/create-crm-note.md) | `POST /v3/crm/notes` | [docs](https://developers.brevo.com/reference/createanote) |
| [Create CRM Task](actions/create-crm-task.md) | `POST /v3/crm/tasks` | [docs](https://developers.brevo.com/reference/createatask) |
| [Create Deal](actions/create-deal.md) | `POST /v3/crm/deals` | [docs](https://developers.brevo.com/reference/createadeal) |
| [Create Email Campaign](actions/create-email-campaign.md) | `POST /v3/emailCampaigns` | [docs](https://developers.brevo.com/reference/create-email-campaign) |
| [Create Event](actions/create-event.md) | `POST /v3/events` | [docs](https://developers.brevo.com/reference/createevent) |
| [Create Events Batch](actions/create-events-batch.md) | `POST /v3/events/batch` | [docs](https://developers.brevo.com/reference/createbatchevents) |
| [Create Feed](actions/create-feed.md) | `POST /v3/feeds` | [docs](https://developers.brevo.com/reference/createexternalfeed) |
| [Create List](actions/create-list.md) | `POST /v3/contacts/lists` | [docs](https://developers.brevo.com/reference/create-list) |
| [Create Loyalty Balance Definition](actions/create-loyalty-balance-definition.md) | `POST /v3/loyalty/balance/programs/:pid/balance-definitions` | [docs](https://developers.brevo.com/reference/createbalancedefinition) |
| [Create Loyalty Balance Limit](actions/create-loyalty-balance-limit.md) | `POST /v3/loyalty/balance/programs/:pid/balance-definitions/:bdid/limits` | [docs](https://developers.brevo.com/reference/createbalancelimit) |
| [Create Loyalty Order](actions/create-loyalty-order.md) | `POST /v3/loyalty/balance/programs/:pid/create-order` | [docs](https://developers.brevo.com/reference/createloyaltyorder) |
| [Create Loyalty Program](actions/create-loyalty-program.md) | `POST /v3/loyalty/config/programs` | [docs](https://developers.brevo.com/reference/createnewlp) |
| [Create Loyalty Reward](actions/create-loyalty-reward.md) | `POST /v3/loyalty/offer/programs/:pid/offers` | [docs](https://developers.brevo.com/reference/createreward) |
| [Create Loyalty Subscription Balances](actions/create-loyalty-subscription-balances.md) | `POST /v3/loyalty/balance/programs/:pid/subscriptions/:cid/balances` | [docs](https://developers.brevo.com/reference/createbalanceforcontact) |
| [Create Loyalty Subscription Member](actions/create-loyalty-subscription-member.md) | `POST /v3/loyalty/config/programs/:pid/subscription-members` | [docs](https://developers.brevo.com/reference/subscribemembertoasubscription) |
| [Create Loyalty Tier](actions/create-loyalty-tier.md) | `POST /v3/loyalty/tier/programs/:pid/tier-groups/:gid/tiers` | [docs](https://developers.brevo.com/reference/createtierfortiergroup) |
| [Create Loyalty Tier Group](actions/create-loyalty-tier-group.md) | `POST /v3/loyalty/tier/programs/:pid/tier-groups` | [docs](https://developers.brevo.com/reference/createtiergroup) |
| [Create Loyalty Transaction](actions/create-loyalty-transaction.md) | `POST /v3/loyalty/balance/programs/:pid/transactions` | [docs](https://developers.brevo.com/reference/createtransaction) |
| [Create Loyalty Voucher](actions/create-loyalty-voucher.md) | `POST /v3/loyalty/offer/programs/:pid/rewards/attribute` | [docs](https://developers.brevo.com/reference/createvoucher) |
| [Create Order Status](actions/create-order-status.md) | `POST /v3/orders/status` | [docs](https://developers.brevo.com/reference/createorder) |
| [Create Orders Batch](actions/create-orders-batch.md) | `POST /v3/orders/status/batch` | [docs](https://developers.brevo.com/reference/createbatchorder) |
| [Create Payment Request](actions/create-payment-request.md) | `POST /v3/payments/requests` | [docs](https://developers.brevo.com/reference/createpaymentrequest) |
| [Create Product](actions/create-product.md) | `POST /v3/products` | [docs](https://developers.brevo.com/reference/createupdateproduct) |
| [Create Product Alert](actions/create-product-alert.md) | `POST /v3/products/:id/alerts/:type` | [docs](https://developers.brevo.com/reference/createproductalert) |
| [Create Products Batch](actions/create-products-batch.md) | `POST /v3/products/batch` | [docs](https://developers.brevo.com/reference/createupdatebatchproducts) |
| [Create Pushed Conversation Message](actions/create-pushed-conversation-message.md) | `POST /v3/conversations/pushedMessages` | [docs](https://developers.brevo.com/reference/pushamessagetothevisitors) |
| [Create Sender](actions/create-sender.md) | `POST /v3/senders` | [docs](https://developers.brevo.com/reference/createsender) |
| [Create Sender Domain](actions/create-sender-domain.md) | `POST /v3/senders/domains` | [docs](https://developers.brevo.com/reference/createdomain) |
| [Create SMS Campaign](actions/create-sms-campaign.md) | `POST /v3/smsCampaigns` | [docs](https://developers.brevo.com/reference/createsmscampaign) |
| [Create SMTP Template](actions/create-smtp-template.md) | `POST /v3/smtp/templates` | [docs](https://developers.brevo.com/reference/create-smtp-template) |
| [Create Webhook](actions/create-webhook.md) | `POST /v3/webhooks` | [docs](https://developers.brevo.com/reference/create-webhook) |
| [Create WhatsApp Campaign](actions/create-whats-app-campaign.md) | `POST /v3/whatsappCampaigns` | [docs](https://developers.brevo.com/reference/create-and-send-a-whatsapp-campaign) |
| [Create WhatsApp Template](actions/create-whats-app-template.md) | `POST /v3/whatsappCampaigns/template` | [docs](https://developers.brevo.com/reference/create-a-whatsapp-template) |
| [Delete Blocked Contact](actions/delete-blocked-contact.md) | `DELETE /v3/smtp/blockedContacts/:email` | [docs](https://developers.brevo.com/reference/unblock-or-resubscribe-a-transactional-contact) |
| [Delete Blocked Domain](actions/delete-blocked-domain.md) | `DELETE /v3/smtp/blockedDomains/:domain` | [docs](https://developers.brevo.com/reference/deleteblockeddomain) |
| [Delete Company](actions/delete-company.md) | `DELETE /v3/companies/:id` | [docs](https://developers.brevo.com/reference/deleteacompany) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /v3/contacts/:identifier` | [docs](https://developers.brevo.com/reference/delete-contact) |
| [Delete Contact Attribute](actions/delete-contact-attribute.md) | `DELETE /v3/contacts/attributes/:attributeCategory/:attributeName` | [docs](https://developers.brevo.com/reference/delete-attribute) |
| [Delete Contact Attribute Option](actions/delete-contact-attribute-option.md) | `DELETE /v3/contacts/attributes/:attributeType/:multipleChoiceAttribute/:multipleChoiceAttributeOption` | [docs](https://developers.brevo.com/reference/deletemultiattributeoptions) |
| [Delete Contact Folder](actions/delete-contact-folder.md) | `DELETE /v3/contacts/folders/:folderId` | [docs](https://developers.brevo.com/reference/deletefolder) |
| [Delete Conversation Message](actions/delete-conversation-message.md) | `DELETE /v3/conversations/messages/:id` | [docs](https://developers.brevo.com/reference/delete-a-message-sent-by-an-agent) |
| [Delete Corporate Group](actions/delete-corporate-group.md) | `DELETE /v3/corporate/group/:id` | [docs](https://developers.brevo.com/reference/delete-a-group) |
| [Delete Corporate Sub Account](actions/delete-corporate-sub-account.md) | `DELETE /v3/corporate/subAccount/:id` | [docs](https://developers.brevo.com/reference/delete-a-sub-account) |
| [Delete CRM Attribute](actions/delete-crm-attribute.md) | `DELETE /v3/crm/attributes/:id` | [docs](https://developers.brevo.com/reference/delete-an-attribute) |
| [Delete CRM File](actions/delete-crm-file.md) | `DELETE /v3/crm/files/:id` | [docs](https://developers.brevo.com/reference/deleteafile) |
| [Delete CRM Note](actions/delete-crm-note.md) | `DELETE /v3/crm/notes/:id` | [docs](https://developers.brevo.com/reference/deleteanote) |
| [Delete CRM Task](actions/delete-crm-task.md) | `DELETE /v3/crm/tasks/:id` | [docs](https://developers.brevo.com/reference/deleteatask) |
| [Delete Deal](actions/delete-deal.md) | `DELETE /v3/crm/deals/:id` | [docs](https://developers.brevo.com/reference/deleteadeal) |
| [Delete Email Campaign](actions/delete-email-campaign.md) | `DELETE /v3/emailCampaigns/:campaignId` | [docs](https://developers.brevo.com/reference/delete-email-campaign) |
| [Delete Feed](actions/delete-feed.md) | `DELETE /v3/feeds/:uuid` | [docs](https://developers.brevo.com/reference/deleteexternalfeed) |
| [Delete Hard Bounces](actions/delete-hard-bounces.md) | `POST /v3/smtp/deleteHardbounces` | [docs](https://developers.brevo.com/reference/deletehardbounces) |
| [Delete List](actions/delete-list.md) | `DELETE /v3/contacts/lists/:listId` | [docs](https://developers.brevo.com/reference/delete-list) |
| [Delete Loyalty Balance Definition](actions/delete-loyalty-balance-definition.md) | `DELETE /v3/loyalty/balance/programs/:pid/balance-definitions/:bdid` | [docs](https://developers.brevo.com/reference/deletebalancedefinition) |
| [Delete Loyalty Balance Limit](actions/delete-loyalty-balance-limit.md) | `DELETE /v3/loyalty/balance/programs/:pid/balance-definitions/:bdid/limits/:blid` | [docs](https://developers.brevo.com/reference/deletebalancelimit) |
| [Delete Loyalty Contact Subscription](actions/delete-loyalty-contact-subscription.md) | `DELETE /v3/loyalty/config/programs/:pid/contact/:cid` | [docs](https://developers.brevo.com/reference/deletecontactsubscription) |
| [Delete Loyalty Program](actions/delete-loyalty-program.md) | `DELETE /v3/loyalty/config/programs/:pid` | [docs](https://developers.brevo.com/reference/deleteloyaltyprogram) |
| [Delete Loyalty Subscription Members](actions/delete-loyalty-subscription-members.md) | `DELETE /v3/loyalty/config/programs/:pid/subscription-members` | [docs](https://developers.brevo.com/reference/deletecontactmembers) |
| [Delete Loyalty Tier](actions/delete-loyalty-tier.md) | `DELETE /v3/loyalty/tier/programs/:pid/tiers/:tid` | [docs](https://developers.brevo.com/reference/deletetier) |
| [Delete Loyalty Tier Group](actions/delete-loyalty-tier-group.md) | `DELETE /v3/loyalty/tier/programs/:pid/tier-groups/:gid` | [docs](https://developers.brevo.com/reference/deletetiergroup) |
| [Delete Object Records Batch](actions/delete-object-records-batch.md) | `POST /v3/objects/:object_type/batch/delete` | [docs](https://developers.brevo.com/reference/deletebatchrecords) |
| [Delete Payment Request](actions/delete-payment-request.md) | `DELETE /v3/payments/requests/:id` | [docs](https://developers.brevo.com/reference/deletepaymentrequest) |
| [Delete Pushed Conversation Message](actions/delete-pushed-conversation-message.md) | `DELETE /v3/conversations/pushedMessages/:id` | [docs](https://developers.brevo.com/reference/delete-an-automated-message) |
| [Delete Scheduled Email](actions/delete-scheduled-email.md) | `DELETE /v3/smtp/email/:identifier` | [docs](https://developers.brevo.com/reference/deletescheduledemailbyid) |
| [Delete Sender](actions/delete-sender.md) | `DELETE /v3/senders/:senderId` | [docs](https://developers.brevo.com/reference/deletesender) |
| [Delete Sender Domain](actions/delete-sender-domain.md) | `DELETE /v3/senders/domains/:domainName` | [docs](https://developers.brevo.com/reference/deletedomain) |
| [Delete SMS Campaign](actions/delete-sms-campaign.md) | `DELETE /v3/smsCampaigns/:campaignId` | [docs](https://developers.brevo.com/reference/deletesmscampaign) |
| [Delete SMTP Log](actions/delete-smtp-log.md) | `DELETE /v3/smtp/log/:identifier` | [docs](https://developers.brevo.com/reference/delete-an-smtp-transactional-log) |
| [Delete SMTP Template](actions/delete-smtp-template.md) | `DELETE /v3/smtp/templates/:templateId` | [docs](https://developers.brevo.com/reference/delete-smtp-template) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /v3/webhooks/:webhookId` | [docs](https://developers.brevo.com/reference/delete-webhook) |
| [Delete WhatsApp Campaign](actions/delete-whats-app-campaign.md) | `DELETE /v3/whatsappCampaigns/:campaignId` | [docs](https://developers.brevo.com/reference/deletewhatsappcampaign) |
| [Dissociate Corporate Sub Account IP](actions/dissociate-corporate-sub-account-ip.md) | `PUT /v3/corporate/subAccount/ip/dissociate` | [docs](https://developers.brevo.com/reference/dissociate-an-ip-to-sub-accounts) |
| [Export Contacts](actions/export-contacts.md) | `POST /v3/contacts/export` | [docs](https://developers.brevo.com/reference/request-contact-export) |
| [Export Email Campaign Recipients](actions/export-email-campaign-recipients.md) | `POST /v3/emailCampaigns/:campaignId/exportRecipients` | [docs](https://developers.brevo.com/reference/emailexportrecipients) |
| [Export SMS Campaign Recipients](actions/export-sms-campaign-recipients.md) | `POST /v3/smsCampaigns/:campaignId/exportRecipients` | [docs](https://developers.brevo.com/reference/requestsmsrecipientexport) |
| [Export Webhook History](actions/export-webhook-history.md) | `POST /v3/webhooks/export` | [docs](https://developers.brevo.com/reference/exportwebhookshistory) |
| [Get Account](actions/get-account.md) | `GET /v3/account` | [docs](https://developers.brevo.com/reference/get-account) |
| [Get Category](actions/get-category.md) | `GET /v3/categories/:id` | [docs](https://developers.brevo.com/reference/getcategoryinfo) |
| [Get Company](actions/get-company.md) | `GET /v3/companies/:id` | [docs](https://developers.brevo.com/reference/getacompany) |
| [Get Contact](actions/get-contact.md) | `GET /v3/contacts/:identifier` | [docs](https://developers.brevo.com/reference/get-contact-info) |
| [Get Contact Campaign Stats](actions/get-contact-campaign-stats.md) | `GET /v3/contacts/:identifier/campaignStats` | [docs](https://developers.brevo.com/reference/get-contact-stats) |
| [Get Contact Folder](actions/get-contact-folder.md) | `GET /v3/contacts/folders/:folderId` | [docs](https://developers.brevo.com/reference/get-folder) |
| [Get Conversation Message](actions/get-conversation-message.md) | `GET /v3/conversations/messages/:id` | [docs](https://developers.brevo.com/reference/get-a-message) |
| [Get Corporate Group](actions/get-corporate-group.md) | `GET /v3/corporate/group/:id` | [docs](https://developers.brevo.com/reference/get-a-group-details) |
| [Get Corporate Invited User Permissions](actions/get-corporate-invited-user-permissions.md) | `GET /v3/corporate/user/:email/permissions` | [docs](https://developers.brevo.com/reference/getcorporateuserpermission) |
| [Get Corporate Sub Account](actions/get-corporate-sub-account.md) | `GET /v3/corporate/subAccount/:id` | [docs](https://developers.brevo.com/reference/get-sub-account-details) |
| [Get Corporate User Permissions](actions/get-corporate-user-permissions.md) | `GET /v3/corporate/user/:email/permissions` | [docs](https://developers.brevo.com/reference/getcorporateuserpermission) |
| [Get Coupon Collection](actions/get-coupon-collection.md) | `GET /v3/couponCollections/:id` | [docs](https://developers.brevo.com/reference/getcouponcollection) |
| [Get CRM File](actions/get-crm-file.md) | `GET /v3/crm/files/:id` | [docs](https://developers.brevo.com/reference/downloadafile) |
| [Get CRM File Metadata](actions/get-crm-file-metadata.md) | `GET /v3/crm/files/:id/data` | [docs](https://developers.brevo.com/reference/getfiledetails) |
| [Get CRM Note](actions/get-crm-note.md) | `GET /v3/crm/notes/:id` | [docs](https://developers.brevo.com/reference/getanote) |
| [Get CRM Pipeline](actions/get-crm-pipeline.md) | `GET /v3/crm/pipeline/details/:pipelineID` | [docs](https://developers.brevo.com/reference/getapipeline) |
| [Get CRM Task](actions/get-crm-task.md) | `GET /v3/crm/tasks/:id` | [docs](https://developers.brevo.com/reference/getatask) |
| [Get Deal](actions/get-deal.md) | `GET /v3/crm/deals/:id` | [docs](https://developers.brevo.com/reference/getadeal) |
| [Get Ecommerce Attribution Metric Detail](actions/get-ecommerce-attribution-metric-detail.md) | `GET /v3/ecommerce/attribution/metrics/:conversionSource/:conversionSourceId` | [docs](https://developers.brevo.com/reference/get-detailed-attribution-metrics-for-a-single-brevo-campaign-or-workflow) |
| [Get Ecommerce Display Currency](actions/get-ecommerce-display-currency.md) | `GET /v3/ecommerce/config/displayCurrency` | [docs](https://developers.brevo.com/reference/get-the-iso-4217-compliant-display-currency-code-for-your-brevo-account) |
| [Get Email Campaign](actions/get-email-campaign.md) | `GET /v3/emailCampaigns/:campaignId` | [docs](https://developers.brevo.com/reference/get-email-campaign) |
| [Get Email Campaign AB Test Result](actions/get-email-campaign-ab-test-result.md) | `GET /v3/emailCampaigns/:campaignId/abTestCampaignResult` | [docs](https://developers.brevo.com/reference/get-ab-test-campaign-result) |
| [Get Email Campaign Shared URL](actions/get-email-campaign-shared-url.md) | `GET /v3/emailCampaigns/:campaignId/sharedUrl` | [docs](https://developers.brevo.com/reference/get-shared-template-url) |
| [Get Feed](actions/get-feed.md) | `GET /v3/feeds/:uuid` | [docs](https://developers.brevo.com/reference/getexternalfeedbyuuid) |
| [Get Inbound Attachment](actions/get-inbound-attachment.md) | `GET /v3/inbound/attachments/:downloadToken` | [docs](https://developers.brevo.com/reference/getinboundemailattachment) |
| [Get Inbound Event](actions/get-inbound-event.md) | `GET /v3/inbound/events/:uuid` | [docs](https://developers.brevo.com/reference/getinboundemaileventbyuuid) |
| [Get List](actions/get-list.md) | `GET /v3/contacts/lists/:listId` | [docs](https://developers.brevo.com/reference/get-list) |
| [Get Loyalty Active Balances](actions/get-loyalty-active-balances.md) | `GET /v3/loyalty/balance/programs/:pid/active-balance` | [docs](https://developers.brevo.com/reference/get-active-balances-api) |
| [Get Loyalty Balance Definition](actions/get-loyalty-balance-definition.md) | `GET /v3/loyalty/balance/programs/:pid/balance-definitions/:bdid` | [docs](https://developers.brevo.com/reference/getbalancedefinition) |
| [Get Loyalty Balance Limit](actions/get-loyalty-balance-limit.md) | `GET /v3/loyalty/balance/programs/:pid/balance-definitions/:bdid/limits/:blid` | [docs](https://developers.brevo.com/reference/getbalancelimit) |
| [Get Loyalty Code Count](actions/get-loyalty-code-count.md) | `GET /v3/loyalty/offer/programs/:pid/code-pools/:cpid/codes-count` | [docs](https://developers.brevo.com/reference/getcodecount) |
| [Get Loyalty Offers](actions/get-loyalty-offers.md) | `GET /v3/loyalty/offer/programs/:pid/offers` | [docs](https://developers.brevo.com/reference/get-reward-page-api) |
| [Get Loyalty Program](actions/get-loyalty-program.md) | `GET /v3/loyalty/config/programs/:pid` | [docs](https://developers.brevo.com/reference/getloyaltyprograminfo) |
| [Get Loyalty Programs](actions/get-loyalty-programs.md) | `GET /v3/loyalty/config/programs` | [docs](https://developers.brevo.com/reference/getlplist) |
| [Get Loyalty Reward](actions/get-loyalty-reward.md) | `GET /v3/loyalty/offer/programs/:pid/rewards/:rid` | [docs](https://developers.brevo.com/reference/get-reward-information) |
| [Get Loyalty Subscription Balances](actions/get-loyalty-subscription-balances.md) | `GET /v3/loyalty/balance/programs/:pid/subscriptions/:cid/balances` | [docs](https://developers.brevo.com/reference/getsubscriptionbalances) |
| [Get Loyalty Subscription Data](actions/get-loyalty-subscription-data.md) | `GET /v3/loyalty/config/programs/:pid/account-info` | [docs](https://developers.brevo.com/reference/getparametersubscriptioninfo) |
| [Get Loyalty Tier Group](actions/get-loyalty-tier-group.md) | `GET /v3/loyalty/tier/programs/:pid/tier-groups/:gid` | [docs](https://developers.brevo.com/reference/gettiergroup) |
| [Get Loyalty Vouchers](actions/get-loyalty-vouchers.md) | `GET /v3/loyalty/offer/programs/:pid/vouchers` | [docs](https://developers.brevo.com/reference/get-voucher-for-a-contact) |
| [Get Master Account](actions/get-master-account.md) | `GET /v3/corporate/masterAccount` | [docs](https://developers.brevo.com/reference/get-the-details-of-requested-master-account) |
| [Get Organization User Permissions](actions/get-organization-user-permissions.md) | `GET /v3/organization/user/:email/permissions` | [docs](https://developers.brevo.com/reference/getuserpermission) |
| [Get Payment Request](actions/get-payment-request.md) | `GET /v3/payments/requests/:id` | [docs](https://developers.brevo.com/reference/getpaymentrequest) |
| [Get Process](actions/get-process.md) | `GET /v3/processes/:processId` | [docs](https://developers.brevo.com/reference/getprocess) |
| [Get Product](actions/get-product.md) | `GET /v3/products/:id` | [docs](https://developers.brevo.com/reference/getproductinfo) |
| [Get Pushed Conversation Message](actions/get-pushed-conversation-message.md) | `GET /v3/conversations/pushedMessages/:id` | [docs](https://developers.brevo.com/reference/get-an-automated-message) |
| [Get Scheduled Email](actions/get-scheduled-email.md) | `GET /v3/smtp/emailStatus/:identifier` | [docs](https://developers.brevo.com/reference/getscheduledemailbyid) |
| [Get Sender Domain](actions/get-sender-domain.md) | `GET /v3/senders/domains/:domainName` | [docs](https://developers.brevo.com/reference/getdomainconfiguration) |
| [Get SMS Campaign](actions/get-sms-campaign.md) | `GET /v3/smsCampaigns/:campaignId` | [docs](https://developers.brevo.com/reference/getsmscampaign) |
| [Get SMTP Aggregated Report](actions/get-smtp-aggregated-report.md) | `GET /v3/smtp/statistics/aggregatedReport` | [docs](https://developers.brevo.com/reference/getaggregatedsmtpreport) |
| [Get SMTP Template](actions/get-smtp-template.md) | `GET /v3/smtp/templates/:templateId` | [docs](https://developers.brevo.com/reference/get-smtp-template) |
| [Get Transactional Email Content](actions/get-transactional-email-content.md) | `GET /v3/smtp/emails/:uuid` | [docs](https://developers.brevo.com/reference/gettransacemailcontent) |
| [Get Transactional SMS Aggregated Report](actions/get-transactional-sms-aggregated-report.md) | `GET /v3/transactionalSMS/statistics/aggregatedReport` | [docs](https://developers.brevo.com/reference/gettransacaggregatedsmsreport) |
| [Get Webhook](actions/get-webhook.md) | `GET /v3/webhooks/:webhookId` | [docs](https://developers.brevo.com/reference/get-webhook) |
| [Get WhatsApp Campaign](actions/get-whats-app-campaign.md) | `GET /v3/whatsappCampaigns/:campaignId` | [docs](https://developers.brevo.com/reference/getwhatsappcampaign) |
| [Get WhatsApp Campaign Config](actions/get-whats-app-campaign-config.md) | `GET /v3/whatsappCampaigns/config` | [docs](https://developers.brevo.com/reference/getwhatsappcampaignsconfig) |
| [Import Companies](actions/import-companies.md) | `POST /v3/companies/import` | [docs](https://developers.brevo.com/reference/import-companiescreation-and-updation) |
| [Import Contacts](actions/import-contacts.md) | `POST /v3/contacts/import` | [docs](https://developers.brevo.com/reference/import-contacts) |
| [Import Deals](actions/import-deals.md) | `POST /v3/crm/deals/import` | [docs](https://developers.brevo.com/reference/import-dealscreation-and-updation) |
| [Invite Corporate Admin User](actions/invite-corporate-admin-user.md) | `POST /v3/corporate/user/invitation/send` | [docs](https://developers.brevo.com/reference/inviteadminuser) |
| [Invite Organization User](actions/invite-organization-user.md) | `POST /v3/organization/user/invitation/send` | [docs](https://developers.brevo.com/reference/inviteuser) |
| [Link Unlink Company](actions/link-unlink-company.md) | `PATCH /v3/companies/link-unlink/:id` | [docs](https://developers.brevo.com/reference/link-and-unlink-company-with-contact-and-deal) |
| [Link Unlink Deal](actions/link-unlink-deal.md) | `PATCH /v3/crm/deals/link-unlink/:id` | [docs](https://developers.brevo.com/reference/link-and-unlink-a-deal-with-contacts-and-companies) |
| [List Blocked Contacts](actions/list-blocked-contacts.md) | `GET /v3/smtp/blockedContacts` | [docs](https://developers.brevo.com/reference/gettransacblockedcontacts) |
| [List Blocked Domains](actions/list-blocked-domains.md) | `GET /v3/smtp/blockedDomains` | [docs](https://developers.brevo.com/reference/getblockeddomains) |
| [List Categories](actions/list-categories.md) | `GET /v3/categories` | [docs](https://developers.brevo.com/reference/getcategories) |
| [List Companies](actions/list-companies.md) | `GET /v3/companies` | [docs](https://developers.brevo.com/reference/getallcompanies) |
| [List Contact Attributes](actions/list-contact-attributes.md) | `GET /v3/contacts/attributes` | [docs](https://developers.brevo.com/reference/get-attributes) |
| [List Contact Folders](actions/list-contact-folders.md) | `GET /v3/contacts/folders` | [docs](https://developers.brevo.com/reference/get-folders) |
| [List Contacts](actions/list-contacts.md) | `GET /v3/contacts` | [docs](https://developers.brevo.com/reference/get-contacts) |
| [List Contacts in List](actions/list-contacts-in-list.md) | `GET /v3/contacts/lists/:listId/contacts` | [docs](https://developers.brevo.com/reference/get-contacts-from-list) |
| [List Corporate Groups](actions/list-corporate-groups.md) | `GET /v3/corporate/groups` | [docs](https://developers.brevo.com/reference/getsubaccountgroups) |
| [List Corporate IPs](actions/list-corporate-i-ps.md) | `GET /v3/corporate/ip` | [docs](https://developers.brevo.com/reference/list-of-all-ips) |
| [List Corporate Invited Users](actions/list-corporate-invited-users.md) | `GET /v3/corporate/invited/users` | [docs](https://developers.brevo.com/reference/getcorporateinviteduserslist) |
| [List Corporate Sub Accounts](actions/list-corporate-sub-accounts.md) | `GET /v3/corporate/subAccount` | [docs](https://developers.brevo.com/reference/get-the-list-of-all-the-sub-accounts-of-the-master-account) |
| [List Coupon Collections](actions/list-coupon-collections.md) | `GET /v3/couponCollections` | [docs](https://developers.brevo.com/reference/getcouponcollections) |
| [List CRM Company Attributes](actions/list-crm-company-attributes.md) | `GET /v3/crm/attributes/companies` | [docs](https://developers.brevo.com/reference/getcompanyattributes) |
| [List CRM Deal Attributes](actions/list-crm-deal-attributes.md) | `GET /v3/crm/attributes/deals` | [docs](https://developers.brevo.com/reference/getdealattributes) |
| [List CRM Files](actions/list-crm-files.md) | `GET /v3/crm/files` | [docs](https://developers.brevo.com/reference/getallfiles) |
| [List CRM Notes](actions/list-crm-notes.md) | `GET /v3/crm/notes` | [docs](https://developers.brevo.com/reference/getallnotes) |
| [List CRM Pipeline Details](actions/list-crm-pipeline-details.md) | `GET /v3/crm/pipeline/details` | [docs](https://developers.brevo.com/reference/getallpipelinedetails) |
| [List CRM Pipelines](actions/list-crm-pipelines.md) | `GET /v3/crm/pipeline/details/all` | [docs](https://developers.brevo.com/reference/getallpipelines) |
| [List CRM Task Types](actions/list-crm-task-types.md) | `GET /v3/crm/tasktypes` | [docs](https://developers.brevo.com/reference/getalltasktypes) |
| [List CRM Tasks](actions/list-crm-tasks.md) | `GET /v3/crm/tasks` | [docs](https://developers.brevo.com/reference/getalltasks) |
| [List Deals](actions/list-deals.md) | `GET /v3/crm/deals` | [docs](https://developers.brevo.com/reference/getalldeals) |
| [List Ecommerce Attributed Products](actions/list-ecommerce-attributed-products.md) | `GET /v3/ecommerce/attribution/products/:conversionSource/:conversionSourceId` | [docs](https://developers.brevo.com/reference/get-attributed-product-sales-for-a-single-brevo-campaign-or-workflow) |
| [List Ecommerce Attribution Metrics](actions/list-ecommerce-attribution-metrics.md) | `GET /v3/ecommerce/attribution/metrics` | [docs](https://developers.brevo.com/reference/get-attribution-metrics-for-one-or-more-brevo-campaigns-or-workflows) |
| [List Email Campaigns](actions/list-email-campaigns.md) | `GET /v3/emailCampaigns` | [docs](https://developers.brevo.com/reference/get-email-campaigns) |
| [List Events](actions/list-events.md) | `GET /v3/events` | [docs](https://developers.brevo.com/reference/getevents) |
| [List Feeds](actions/list-feeds.md) | `GET /v3/feeds` | [docs](https://developers.brevo.com/reference/getallexternalfeeds) |
| [List Inbound Events](actions/list-inbound-events.md) | `GET /v3/inbound/events` | [docs](https://developers.brevo.com/reference/getinboundemailevents) |
| [List Lists](actions/list-lists.md) | `GET /v3/contacts/lists` | [docs](https://developers.brevo.com/reference/get-lists) |
| [List Lists in Folder](actions/list-lists-in-folder.md) | `GET /v3/contacts/folders/:folderId/lists` | [docs](https://developers.brevo.com/reference/get-folder-lists) |
| [List Loyalty Balance Definitions](actions/list-loyalty-balance-definitions.md) | `GET /v3/loyalty/balance/programs/:pid/balance-definitions` | [docs](https://developers.brevo.com/reference/getbalancedefinitionlist) |
| [List Loyalty Contact Balances](actions/list-loyalty-contact-balances.md) | `GET /v3/loyalty/balance/programs/:pid/contact-balances` | [docs](https://developers.brevo.com/reference/getcontactbalances) |
| [List Loyalty Tier Groups](actions/list-loyalty-tier-groups.md) | `GET /v3/loyalty/tier/programs/:pid/tier-groups` | [docs](https://developers.brevo.com/reference/getlistoftiergroups) |
| [List Loyalty Tiers](actions/list-loyalty-tiers.md) | `GET /v3/loyalty/tier/programs/:pid/tiers` | [docs](https://developers.brevo.com/reference/getloyaltyprogramtier) |
| [List Loyalty Transaction History](actions/list-loyalty-transaction-history.md) | `GET /v3/loyalty/balance/programs/:pid/transaction-history` | [docs](https://developers.brevo.com/reference/gettransactionhistory) |
| [List Object Records](actions/list-object-records.md) | `GET /v3/objects/:object_type/records` | [docs](https://developers.brevo.com/reference/getrecords) |
| [List Orders](actions/list-orders.md) | `GET /v3/orders` | [docs](https://developers.brevo.com/reference/getorders) |
| [List Organization Activities](actions/list-organization-activities.md) | `GET /v3/organization/activities` | [docs](https://developers.brevo.com/reference/getaccountactivity) |
| [List Organization Invited Users](actions/list-organization-invited-users.md) | `GET /v3/organization/invited/users` | [docs](https://developers.brevo.com/reference/getinviteduserslist) |
| [List Processes](actions/list-processes.md) | `GET /v3/processes` | [docs](https://developers.brevo.com/reference/getprocesses) |
| [List Products](actions/list-products.md) | `GET /v3/products` | [docs](https://developers.brevo.com/reference/getproducts) |
| [List Segments](actions/list-segments.md) | `GET /v3/contacts/segments` | [docs](https://developers.brevo.com/reference/get-segments) |
| [List Sender Domains](actions/list-sender-domains.md) | `GET /v3/senders/domains` | [docs](https://developers.brevo.com/reference/getdomains) |
| [List Sender IPs](actions/list-sender-i-ps.md) | `GET /v3/senders/ips` | [docs](https://developers.brevo.com/reference/getips) |
| [List Sender IPs by Sender](actions/list-sender-i-ps-by-sender.md) | `GET /v3/senders/:senderId/ips` | [docs](https://developers.brevo.com/reference/getipsfromsender) |
| [List Senders](actions/list-senders.md) | `GET /v3/senders` | [docs](https://developers.brevo.com/reference/get-senders) |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | `GET /v3/smsCampaigns` | [docs](https://developers.brevo.com/reference/getsmscampaigns) |
| [List SMS Templates](actions/list-sms-templates.md) | `GET /v3/transactionalSMS/templates` | [docs](https://developers.brevo.com/reference/getsmstemplates) |
| [List SMTP Events](actions/list-smtp-events.md) | `GET /v3/smtp/statistics/events` | [docs](https://developers.brevo.com/reference/getsmtpevents) |
| [List SMTP Reports](actions/list-smtp-reports.md) | `GET /v3/smtp/statistics/reports` | [docs](https://developers.brevo.com/reference/getsmtpreports) |
| [List SMTP Templates](actions/list-smtp-templates.md) | `GET /v3/smtp/templates` | [docs](https://developers.brevo.com/reference/get-smtp-templates) |
| [List Transactional Emails](actions/list-transactional-emails.md) | `GET /v3/smtp/emails` | [docs](https://developers.brevo.com/reference/get-transac-emails-list) |
| [List Transactional SMS Events](actions/list-transactional-sms-events.md) | `GET /v3/transactionalSMS/statistics/events` | [docs](https://developers.brevo.com/reference/getsmsevents) |
| [List Transactional SMS Reports](actions/list-transactional-sms-reports.md) | `GET /v3/transactionalSMS/statistics/reports` | [docs](https://developers.brevo.com/reference/gettransacsmsreport) |
| [List Webhooks](actions/list-webhooks.md) | `GET /v3/webhooks` | [docs](https://developers.brevo.com/reference/get-webhooks) |
| [List WhatsApp Campaigns](actions/list-whats-app-campaigns.md) | `GET /v3/whatsappCampaigns` | [docs](https://developers.brevo.com/reference/getwhatsappcampaigns) |
| [List WhatsApp Events](actions/list-whats-app-events.md) | `GET /v3/whatsapp/statistics/events` | [docs](https://developers.brevo.com/reference/getwhatsappeventreport) |
| [List WhatsApp Templates](actions/list-whats-app-templates.md) | `GET /v3/whatsappCampaigns/template-list` | [docs](https://developers.brevo.com/reference/getwhatsappcampaignstemplatelist) |
| [Partially Update Loyalty Program](actions/partially-update-loyalty-program.md) | `PATCH /v3/loyalty/config/programs/:pid` | [docs](https://developers.brevo.com/reference/partiallyupdateloyaltyprogram) |
| [Ping Conversation Agent Online](actions/ping-conversation-agent-online.md) | `POST /v3/conversations/agentOnlinePing` | [docs](https://developers.brevo.com/reference/sets-agents-status-to-online-for-2-3-minutes) |
| [Preview SMTP Template](actions/preview-smtp-template.md) | `POST /v3/smtp/template/preview` | [docs](https://developers.brevo.com/reference/postpreviewsmtpemailtemplates) |
| [Publish Loyalty Program](actions/publish-loyalty-program.md) | `POST /v3/loyalty/config/programs/:pid/publish` | [docs](https://developers.brevo.com/reference/publishloyaltyprogram) |
| [Redeem Loyalty Voucher](actions/redeem-loyalty-voucher.md) | `POST /v3/loyalty/offer/programs/:pid/rewards/redeem` | [docs](https://developers.brevo.com/reference/redeemvoucher) |
| [Remove Contacts from List](actions/remove-contacts-from-list.md) | `POST /v3/contacts/lists/:listId/contacts/remove` | [docs](https://developers.brevo.com/reference/remove-contact-from-list) |
| [Revoke Corporate User](actions/revoke-corporate-user.md) | `DELETE /v3/corporate/user/revoke/:email` | [docs](https://developers.brevo.com/reference/revoke-an-admin-user) |
| [Revoke Loyalty Vouchers](actions/revoke-loyalty-vouchers.md) | `DELETE /v3/loyalty/offer/programs/:pid/rewards/revoke` | [docs](https://developers.brevo.com/reference/revokevouchers) |
| [Revoke Organization User Permission](actions/revoke-organization-user-permission.md) | `PUT /v3/organization/user/invitation/revoke/:email` | [docs](https://developers.brevo.com/reference/putrevokeuserpermission) |
| [Send Async Transactional SMS](actions/send-async-transactional-sms.md) | `POST /v3/transactionalSMS/send` | [docs](https://developers.brevo.com/reference/sendasynctransactionalsms) |
| [Send Double Opt-In Confirmation](actions/send-double-opt-in-confirmation.md) | `POST /v3/contacts/doubleOptinConfirmation` | [docs](https://developers.brevo.com/reference/createdoubleoptincontact) |
| [Send Email Campaign Now](actions/send-email-campaign-now.md) | `POST /v3/emailCampaigns/:campaignId/sendNow` | [docs](https://developers.brevo.com/reference/sendcampaignnow) |
| [Send Email Campaign Report](actions/send-email-campaign-report.md) | `POST /v3/emailCampaigns/:campaignId/sendReport` | [docs](https://developers.brevo.com/reference/sendreport) |
| [Send Email Campaign Test](actions/send-email-campaign-test.md) | `POST /v3/emailCampaigns/:campaignId/sendTest` | [docs](https://developers.brevo.com/reference/sendtestemailtocampaign) |
| [Send SMS Campaign Now](actions/send-sms-campaign-now.md) | `POST /v3/smsCampaigns/:campaignId/sendNow` | [docs](https://developers.brevo.com/reference/sendsmscampaignnow) |
| [Send SMS Campaign Report](actions/send-sms-campaign-report.md) | `POST /v3/smsCampaigns/:campaignId/sendReport` | [docs](https://developers.brevo.com/reference/sendsmsreport) |
| [Send SMS Campaign Test](actions/send-sms-campaign-test.md) | `POST /v3/smsCampaigns/:campaignId/sendTest` | [docs](https://developers.brevo.com/reference/sendtestsms) |
| [Send SMTP Template Test](actions/send-smtp-template-test.md) | `POST /v3/smtp/templates/:templateId/sendTest` | [docs](https://developers.brevo.com/reference/sendtesttemplate) |
| [Send Transactional Email](actions/send-transactional-email.md) | `POST /v3/smtp/email` | [docs](https://developers.brevo.com/reference/sendtransacemail) |
| [Send Transactional SMS](actions/send-transactional-sms.md) | `POST /v3/transactionalSMS/sms` | [docs](https://developers.brevo.com/reference/sendtransacsms) |
| [Send WhatsApp Message](actions/send-whats-app-message.md) | `POST /v3/whatsapp/sendMessage` | [docs](https://developers.brevo.com/reference/sendwhatsappmessage) |
| [Send WhatsApp Template Approval](actions/send-whats-app-template-approval.md) | `POST /v3/whatsappCampaigns/template/approval/:templateId` | [docs](https://developers.brevo.com/reference/send-your-whatsapp-template-for-approval) |
| [Subscribe Loyalty Program](actions/subscribe-loyalty-program.md) | `POST /v3/loyalty/config/programs/:pid/subscriptions` | [docs](https://developers.brevo.com/reference/subscribetoloyaltyprogram) |
| [Toggle Corporate Sub Account Applications](actions/toggle-corporate-sub-account-applications.md) | `PUT /v3/corporate/subAccount/:id/applications/toggle` | [docs](https://developers.brevo.com/reference/enable-disable-sub-account-applications) |
| [Unlink Corporate Group Sub Accounts](actions/unlink-corporate-group-sub-accounts.md) | `PUT /v3/corporate/group/unlink/:groupId/subAccounts` | [docs](https://developers.brevo.com/reference/delete-sub-account-from-group) |
| [Update Company](actions/update-company.md) | `PATCH /v3/companies/:id` | [docs](https://developers.brevo.com/reference/updateacompany) |
| [Update Contact](actions/update-contact.md) | `PUT /v3/contacts/:identifier` | [docs](https://developers.brevo.com/reference/update-contact) |
| [Update Contact Attribute](actions/update-contact-attribute.md) | `PUT /v3/contacts/attributes/:attributeCategory/:attributeName` | [docs](https://developers.brevo.com/reference/update-attribute) |
| [Update Contact Folder](actions/update-contact-folder.md) | `PUT /v3/contacts/folders/:folderId` | [docs](https://developers.brevo.com/reference/updatefolder) |
| [Update Conversation Message](actions/update-conversation-message.md) | `PUT /v3/conversations/messages/:id` | [docs](https://developers.brevo.com/reference/updateamessageasagent) |
| [Update Conversation Visitor Group](actions/update-conversation-visitor-group.md) | `PUT /v3/conversations/visitorGroup` | [docs](https://developers.brevo.com/reference/setvisitorgroup) |
| [Update Corporate Group](actions/update-corporate-group.md) | `PUT /v3/corporate/group/:id` | [docs](https://developers.brevo.com/reference/update-a-group-of-sub-accounts) |
| [Update Corporate Sub Account Plan](actions/update-corporate-sub-account-plan.md) | `PUT /v3/corporate/subAccount/:id/plan` | [docs](https://developers.brevo.com/reference/update-sub-account-plan) |
| [Update Corporate Sub Accounts Plan](actions/update-corporate-sub-accounts-plan.md) | `PUT /v3/corporate/subAccounts/plan` | [docs](https://developers.brevo.com/reference/update-sub-accounts-plan) |
| [Update Corporate User Invitation](actions/update-corporate-user-invitation.md) | `PUT /v3/corporate/user/invitation/:action/:email` | [docs](https://developers.brevo.com/reference/resend-cancel-admin-user-invitation) |
| [Update Corporate User Permissions](actions/update-corporate-user-permissions.md) | `PUT /v3/corporate/user/:email/permissions` | [docs](https://developers.brevo.com/reference/change-admin-user-permissions) |
| [Update Coupon Collection](actions/update-coupon-collection.md) | `PATCH /v3/couponCollections/:id` | [docs](https://developers.brevo.com/reference/updatecouponcollection) |
| [Update CRM Attribute](actions/update-crm-attribute.md) | `PATCH /v3/crm/attributes/:id` | [docs](https://developers.brevo.com/reference/update-an-attribute) |
| [Update CRM Note](actions/update-crm-note.md) | `PATCH /v3/crm/notes/:id` | [docs](https://developers.brevo.com/reference/updateanote) |
| [Update CRM Task](actions/update-crm-task.md) | `PATCH /v3/crm/tasks/:id` | [docs](https://developers.brevo.com/reference/updateatask) |
| [Update Deal](actions/update-deal.md) | `PATCH /v3/crm/deals/:id` | [docs](https://developers.brevo.com/reference/updateadeal) |
| [Update Ecommerce Display Currency](actions/update-ecommerce-display-currency.md) | `POST /v3/ecommerce/config/displayCurrency` | [docs](https://developers.brevo.com/reference/updateecommercedisplaycurrency) |
| [Update Email Campaign](actions/update-email-campaign.md) | `PUT /v3/emailCampaigns/:campaignId` | [docs](https://developers.brevo.com/reference/update-email-campaign) |
| [Update Email Campaign Status](actions/update-email-campaign-status.md) | `PUT /v3/emailCampaigns/:campaignId/status` | [docs](https://developers.brevo.com/reference/updatecampaignstatus) |
| [Update Feed](actions/update-feed.md) | `PUT /v3/feeds/:uuid` | [docs](https://developers.brevo.com/reference/updateexternalfeed) |
| [Update List](actions/update-list.md) | `PUT /v3/contacts/lists/:listId` | [docs](https://developers.brevo.com/reference/update-list) |
| [Update Loyalty Balance Definition](actions/update-loyalty-balance-definition.md) | `PUT /v3/loyalty/balance/programs/:pid/balance-definitions/:bdid` | [docs](https://developers.brevo.com/reference/updatebalancedefinition) |
| [Update Loyalty Balance Limit](actions/update-loyalty-balance-limit.md) | `PUT /v3/loyalty/balance/programs/:pid/balance-definitions/:bdid/limits/:blid` | [docs](https://developers.brevo.com/reference/updatebalancelimit) |
| [Update Loyalty Program](actions/update-loyalty-program.md) | `PUT /v3/loyalty/config/programs/:pid` | [docs](https://developers.brevo.com/reference/updateloyaltyprogram) |
| [Update Loyalty Tier](actions/update-loyalty-tier.md) | `PUT /v3/loyalty/tier/programs/:pid/tiers/:tid` | [docs](https://developers.brevo.com/reference/updatetier) |
| [Update Loyalty Tier Group](actions/update-loyalty-tier-group.md) | `PUT /v3/loyalty/tier/programs/:pid/tier-groups/:gid` | [docs](https://developers.brevo.com/reference/updatetiergroup) |
| [Update Organization User Invitation](actions/update-organization-user-invitation.md) | `PUT /v3/organization/user/invitation/:action/:email` | [docs](https://developers.brevo.com/reference/putresendcancelinvitation) |
| [Update Organization User Permissions](actions/update-organization-user-permissions.md) | `POST /v3/organization/user/update/permissions` | [docs](https://developers.brevo.com/reference/edituserpermission) |
| [Update Pushed Conversation Message](actions/update-pushed-conversation-message.md) | `PUT /v3/conversations/pushedMessages/:id` | [docs](https://developers.brevo.com/reference/updateapushedmessage) |
| [Update Sender](actions/update-sender.md) | `PUT /v3/senders/:senderId` | [docs](https://developers.brevo.com/reference/updatesender) |
| [Update SMS Campaign](actions/update-sms-campaign.md) | `PUT /v3/smsCampaigns/:campaignId` | [docs](https://developers.brevo.com/reference/updatesmscampaign) |
| [Update SMS Campaign Status](actions/update-sms-campaign-status.md) | `PUT /v3/smsCampaigns/:campaignId/status` | [docs](https://developers.brevo.com/reference/updatesmscampaignstatus) |
| [Update SMTP Template](actions/update-smtp-template.md) | `PUT /v3/smtp/templates/:templateId` | [docs](https://developers.brevo.com/reference/update-smtp-template) |
| [Update Webhook](actions/update-webhook.md) | `PUT /v3/webhooks/:webhookId` | [docs](https://developers.brevo.com/reference/update-webhook) |
| [Update WhatsApp Campaign](actions/update-whats-app-campaign.md) | `PUT /v3/whatsappCampaigns/:campaignId` | [docs](https://developers.brevo.com/reference/update-a-whatsapp-campaign) |
| [Upload Email Campaign Image](actions/upload-email-campaign-image.md) | `POST /v3/emailCampaigns/images` | [docs](https://developers.brevo.com/reference/uploadimagetogallery) |
| [Upsert Object Records Batch](actions/upsert-object-records-batch.md) | `POST /v3/objects/:object_type/batch/upsert` | [docs](https://developers.brevo.com/reference/upsertbatchrecords) |
| [Validate Loyalty Reward](actions/validate-loyalty-reward.md) | `POST /v3/loyalty/offer/programs/:pid/rewards/validate` | [docs](https://developers.brevo.com/reference/validatereward) |
| [Validate Sender](actions/validate-sender.md) | `PUT /v3/senders/:senderId/validate` | [docs](https://developers.brevo.com/reference/validatesender) |
