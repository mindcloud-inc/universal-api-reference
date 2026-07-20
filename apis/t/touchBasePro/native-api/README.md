# TouchBasePro: Native API Reference

A consolidated summary of TouchBasePro's API configuration and 124 documented operations, with links to official documentation.

- **Official docs:** https://developer.touchbasepro.com/apis
- **API base URL:** `https://api.touchbasepro.com`

## Authentication

### API Key

Use a TouchBasePro developer portal API/subscription key. Official public docs conflict on whether it is sent as `Authorization: Bearer <API_KEY>` or as the subscription key parameter (`Ocp-Apim-Subscription-Key` / `subscription-key`). Password is not documented in the exported API specs.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://developer.touchbasepro.com/api-details#api=email-validation)

## Endpoints (124 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Activate Webhook](actions/activate-webhook.md) | `PUT /email/lists/{listId}/webhooks/{webhookId}/activate` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Add Rule Group To Segment](actions/add-rule-group-to-segment.md) | `POST /email/segments/{segmentId}/rules` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Create Campaign From Template](actions/create-campaign-from-template.md) | `POST /email/campaigns/fromtemplate` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Create Custom Field](actions/create-custom-field.md) | `POST /email/lists/{listId}/customfields` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Create Draft Campaign](actions/create-draft-campaign.md) | `POST /email/campaigns` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Create Email List](actions/create-email-list.md) | `POST /email/lists` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Create Email Subscriber](actions/create-email-subscriber.md) | `POST /email/subscribers/{listId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Create Email Template](actions/create-email-template.md) | `POST /email/templates` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Create Segment](actions/create-segment.md) | `POST /email/segments/{listId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Create SMS Campaign Webhook](actions/create-sms-campaign-webhook.md) | `POST /sms/campaigns/{campaignId}/webhooks` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Create SMS List](actions/create-sms-list.md) | `POST /sms/lists` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Create SMS List Webhook](actions/create-sms-list-webhook.md) | `POST /sms/lists/{listId}/webhooks` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Create SMS Message Webhook](actions/create-sms-message-webhook.md) | `POST /sms/message/webhooks` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Create SMS Subscriber](actions/create-sms-subscriber.md) | `POST /sms/lists/{listId}/subscribers` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Create Webhook](actions/create-webhook.md) | `POST /email/lists/{listId}/webhooks` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Deactivate Webhook](actions/deactivate-webhook.md) | `PUT /email/lists/{listId}/webhooks/{webhookId}/deactivate` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /email/campaigns/{campaignId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Delete Custom Field](actions/delete-custom-field.md) | `DELETE /email/lists/{listId}/customfields/{customfieldkey}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Delete Email List](actions/delete-email-list.md) | `DELETE /email/lists/{listId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Delete Email Template](actions/delete-email-template.md) | `DELETE /email/templates/{templateId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Delete Segment](actions/delete-segment.md) | `DELETE /email/segments/{segmentId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Delete Segment Rules](actions/delete-segment-rules.md) | `DELETE /email/segments/{segmentId}/rules` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Delete SMS Campaign Webhook](actions/delete-sms-campaign-webhook.md) | `DELETE /sms/campaigns/{campaignId}/webhooks/{webhookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Delete SMS List](actions/delete-sms-list.md) | `DELETE /sms/list/{listId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Delete SMS List Webhook](actions/delete-sms-list-webhook.md) | `DELETE /sms/lists/{listId}/webhooks/{webhookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Delete SMS Message Webhook](actions/delete-sms-message-webhook.md) | `DELETE /sms/message/webhooks/{webhookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Delete SMS Subscriber](actions/delete-sms-subscriber.md) | `DELETE /sms/lists/{listId}/subscribers/{number}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Delete Subscriber](actions/delete-subscriber.md) | `DELETE /email/subscribers/{listId}?email={email}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /email/lists/{listId}/webhooks/{webhookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Download Validation Result](actions/download-validation-result.md) | `GET /validate/DownloadValidationResult?id={id}` | [docs](https://developer.touchbasepro.com/api-details#api=email-validation) |
| [Get Campaign Email Client Usage](actions/get-campaign-email-client-usage.md) | `GET /email/campaigns/{campaignId}/emailclientusage` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Campaign Lists And Segments](actions/get-campaign-lists-and-segments.md) | `GET /email/campaigns/{campaignId}/listsandsegments` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Campaign Summary](actions/get-campaign-summary.md) | `GET /email/campaigns/{campaignId}/summary` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Current Time](actions/get-current-time.md) | `GET /email/systemdate` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Email Client](actions/get-email-client.md) | `GET /email/clients` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Email Credit Balance](actions/get-email-credit-balance.md) | `GET /email/balance` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Email List](actions/get-email-list.md) | `GET /email/lists/{listId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Email Statistics](actions/get-email-statistics.md) | `GET /email/transactional/statistics` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Email Template](actions/get-email-template.md) | `GET /email/templates/{templateId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get List Stats](actions/get-list-stats.md) | `GET /email/lists/{listId}/stats` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Lists For Email](actions/get-lists-for-email.md) | `GET /email/clients/listsforemail?email={email}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Message](actions/get-message.md) | `GET /email/transactional/messages/{messageID}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Message Timeline](actions/get-message-timeline.md) | `GET /email/transactional/messages` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Segment](actions/get-segment.md) | `GET /email/segments/{segmentId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Smart Email Details](actions/get-smart-email-details.md) | `GET /email/transactional/smartEmail/{smartEmailID}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Smart Email List](actions/get-smart-email-list.md) | `GET /email/transactional/smartEmail` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get SMS Campaign](actions/get-sms-campaign.md) | `GET /sms/campaigns/{campaignId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get SMS Campaign Report](actions/get-sms-campaign-report.md) | `GET /sms/campaigns/{campaignId}/report` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get SMS Campaign Webhook](actions/get-sms-campaign-webhook.md) | `GET /sms/campaigns/{campaignId}/webhooks/{webhookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get SMS Credit Balance](actions/get-sms-credit-balance.md) | `GET /sms/balance` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get SMS List](actions/get-sms-list.md) | `GET /sms/lists/{listId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get SMS List Webhook](actions/get-sms-list-webhook.md) | `GET /sms/lists/{listId}/webhooks/{webhookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get SMS Message](actions/get-sms-message.md) | `GET /sms/message/{messageId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get SMS Message Status Webhook](actions/get-sms-message-status-webhook.md) | `GET /sms/message/webhooks/{webhookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get SMS Reply Forward](actions/get-sms-reply-forward.md) | `GET /sms/message/forward` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get SMS Subscriber](actions/get-sms-subscriber.md) | `GET /sms/lists/{listId}/subscribers/{number}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Get Subscriber](actions/get-subscriber.md) | `GET /email/subscribers/{listId}?email={email}&includetrackingpreference={includetrackingpreference}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Subscriber History](actions/get-subscriber-history.md) | `GET /email/subscribers/{listId}/history?email={email}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Suppression List](actions/get-suppression-list.md) | `GET /email/clients/suppressionlist` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Get Validation Credit Balance](actions/get-validation-credit-balance.md) | `GET /validate/balance` | [docs](https://developer.touchbasepro.com/api-details#api=email-validation) |
| [Get Validation List Status](actions/get-validation-list-status.md) | `GET /validate/GetListValidationStatus?RequestId={RequestId}` | [docs](https://developer.touchbasepro.com/api-details#api=email-validation) |
| [Import SMS Subscribers](actions/import-sms-subscribers.md) | `POST /sms/lists/{listId}/subscribers/import` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Import Subscribers](actions/import-subscribers.md) | `POST /email/subscribers/{listId}/import` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Active Subscribers in List](actions/list-active-subscribers-in-list.md) | `GET /email/lists/{listId}/active` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Active Subscribers in Segment](actions/list-active-subscribers-in-segment.md) | `GET /email/segments/{segmentId}/active` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Bounced Subscribers in List](actions/list-bounced-subscribers-in-list.md) | `GET /email/lists/{listId}/bounced` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Campaign Bounces](actions/list-campaign-bounces.md) | `GET /email/campaigns/{campaignId}/bounces` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Campaign Clicks](actions/list-campaign-clicks.md) | `GET /email/campaigns/{campaignId}/clicks` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Campaign Opens](actions/list-campaign-opens.md) | `GET /email/campaigns/{campaignId}/opens` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Campaign Recipients](actions/list-campaign-recipients.md) | `GET /email/campaigns/{campaignId}/recipients` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Campaign Spam Complaints](actions/list-campaign-spam-complaints.md) | `GET /email/campaigns/{campaignId}/spam` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Campaign Unsubscribers](actions/list-campaign-unsubscribers.md) | `GET /email/campaigns/{campaignId}/unsubscribes` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Client Templates](actions/list-client-templates.md) | `GET /email/clients/templates` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Countries](actions/list-countries.md) | `GET /email/countries` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Custom Fields](actions/list-custom-fields.md) | `GET /email/lists/{listId}/customfields` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Deleted Subscribers in List](actions/list-deleted-subscribers-in-list.md) | `GET /email/lists/{listId}/deleted` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Draft Campaigns](actions/list-draft-campaigns.md) | `GET /email/clients/drafts` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Email Client Segments](actions/list-email-client-segments.md) | `GET /email/clients/segments` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Email Lists](actions/list-email-lists.md) | `GET /email/lists` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Scheduled Campaigns](actions/list-scheduled-campaigns.md) | `GET /email/clients/scheduled` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Segments](actions/list-segments.md) | `GET /email/lists/{listId}/segments` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Sent Campaigns](actions/list-sent-campaigns.md) | `GET /email/clients/campaigns` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Smart Email Groups](actions/list-smart-email-groups.md) | `GET /email/transactional/classicEmail/groups` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List SMS Campaign Webhooks](actions/list-sms-campaign-webhooks.md) | `GET /sms/campaigns/{campaignId}/webhooks` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [List SMS Campaigns](actions/list-sms-campaigns.md) | `GET /sms/campaigns?page={page}&pageSize={pageSize}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [List SMS List Webhooks](actions/list-sms-list-webhooks.md) | `GET /sms/lists/{listId}/webhooks` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [List SMS Lists](actions/list-sms-lists.md) | `GET /sms/lists?page={page}&pageSize={pageSize}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [List SMS Message Webhooks](actions/list-sms-message-webhooks.md) | `GET /sms/message/webhooks` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [List SMS Subscribers](actions/list-sms-subscribers.md) | `GET /sms/lists/{listId}/subscribers?page={page}&pageSize={pageSize}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [List Time Zones](actions/list-time-zones.md) | `GET /email/timezones` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Unconfirmed Subscribers in List](actions/list-unconfirmed-subscribers-in-list.md) | `GET /email/lists/{listId}/unconfirmed` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Unsubscribed Subscribers in List](actions/list-unsubscribed-subscribers-in-list.md) | `GET /email/lists/{listId}/unsubscribed` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [List Webhooks](actions/list-webhooks.md) | `GET /email/lists/{listId}/webhooks` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Resend Email Message](actions/resend-email-message.md) | `POST /email/transactional/messages/{messageID}/resend` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Send Campaign Preview](actions/send-campaign-preview.md) | `POST /email/campaigns/{campaignId}/sendpreview` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Send Classic Email](actions/send-classic-email.md) | `POST /email/transactional/classicEmail/send` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Send Draft Campaign](actions/send-draft-campaign.md) | `POST /email/campaigns/{campaignId}/send` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Send Smart Email](actions/send-smart-email.md) | `POST /email/transactional/smartEmail/{smartEmailID}/send` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Send SMS](actions/send-sms.md) | `POST /sms/message` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Set SMS Reply Forward](actions/set-sms-reply-forward.md) | `POST /sms/message/forward` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Suppress Email Addresses](actions/suppress-email-addresses.md) | `POST /email/clients/suppress` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Test Webhook](actions/test-webhook.md) | `GET /email/lists/{listId}/webhooks/{webhookId}/test` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Unschedule Campaign](actions/unschedule-campaign.md) | `POST /email/campaigns/{campaignId}/unschedule` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Unsubscribe Subscriber](actions/unsubscribe-subscriber.md) | `POST /email/subscribers/{listId}/unsubscribe` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Unsuppress Email Address](actions/unsuppress-email-address.md) | `PUT /email/clients/unsuppress?email={email}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Update Custom Field](actions/update-custom-field.md) | `PUT /email/lists/{listId}/customfields/{customfieldkey}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Update Custom Field Options](actions/update-custom-field-options.md) | `PUT /email/lists/{listId}/customfields/{customfieldkey}/options` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Update Email List](actions/update-email-list.md) | `PUT /email/lists/{listId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Update Email Template](actions/update-email-template.md) | `PUT /email/templates/{templateId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Update Segment](actions/update-segment.md) | `PUT /email/segments/{segmentId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Update SMS Campaign Webhook](actions/update-sms-campaign-webhook.md) | `PUT /sms/campaigns/{campaignId}/webhooks/{webhoookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Update SMS List](actions/update-sms-list.md) | `PUT /sms/lists/{listId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Update SMS List Webhook](actions/update-sms-list-webhook.md) | `PUT /sms/lists/{listId}/webhooks/{webhookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Update SMS Message Webhook](actions/update-sms-message-webhook.md) | `PUT /sms/message/webhooks/{webhookId}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Update SMS Subscriber](actions/update-sms-subscriber.md) | `PUT /sms/lists/{listId}/subscribers/{number}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-sms-api) |
| [Update Subscriber](actions/update-subscriber.md) | `PUT /email/subscribers/{listId}?email={email}` | [docs](https://developer.touchbasepro.com/api-details#api=tbp-email-api) |
| [Validate Email Address](actions/validate-email-address.md) | `GET /validate/ValidateEmailAddress?email={email}` | [docs](https://developer.touchbasepro.com/api-details#api=email-validation) |
| [Validate Email List](actions/validate-email-list.md) | `POST /validate/ValidateEmailList` | [docs](https://developer.touchbasepro.com/api-details#api=email-validation) |
| [WhatsApp Create Template](actions/whatsapp-create-template.md) | `POST /whatsapp/v1/public/track/templates/` | [docs](https://developer.touchbasepro.com/api-details#api=whatsapp-api) |
| [WhatsApp Get Users](actions/whatsapp-get-users.md) | `POST /whatsapp/v1/public/apis/users/` | [docs](https://developer.touchbasepro.com/api-details#api=whatsapp-api) |
| [WhatsApp Send Text Message](actions/whatsapp-send-text-message.md) | `POST /whatsapp/v1/public/message/` | [docs](https://developer.touchbasepro.com/api-details#api=whatsapp-api) |
| [WhatsApp Track Events](actions/whatsapp-track-events.md) | `POST /whatsapp/v1/public/track/events/` | [docs](https://developer.touchbasepro.com/api-details#api=whatsapp-api) |
| [WhatsApp Track User](actions/whatsapp-track-user.md) | `POST /whatsapp/v1/public/track/users/` | [docs](https://developer.touchbasepro.com/api-details#api=whatsapp-api) |
| [WhatsApp Upload Media](actions/whatsapp-upload-media.md) | `POST /whatsapp/v1/public/track/files/upload_to_fb/` | [docs](https://developer.touchbasepro.com/api-details#api=whatsapp-api) |
