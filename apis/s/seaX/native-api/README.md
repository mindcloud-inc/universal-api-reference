# SeaX: Native API Reference

A consolidated summary of SeaX's API configuration and 85 documented operations, with links to official documentation.

- **Official docs:** https://api.seasalt.ai/seax/
- **OpenAPI specification:** https://api.seasalt.ai/openapi/seax_openapi.json
- **API base URL:** `https://seax.seasalt.ai/seax-api/api/v1/workspace/{workspaceId}`

## Authentication

### Workspace API Key

Use a SeaX workspace API key plus workspace ID. Requests send the API key in the X-API-Key header and scope every route under the workspace path.

### Credentials

- **API Key:** `apiKey` · required · SeaX Workspace API Key value.
- **Workspace ID:** `workspaceId` · required · SeaX workspace UUID used in every API route.

Send these headers with each API request:

```http
X-API-Key: <apiKey>
```

[Official authentication documentation](https://api.seasalt.ai/seax/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The total page count is read from `total`.

## Pagination

Use `limit` in the query string to set the page size (default 25). Use `offset` in the query string as the record offset; numbering starts at 0.

## Sorting

Set the sort field with `order_by` in the query string. Multiple sort fields can be combined.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (85 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Callback Auto Dialer Campaign Execution](actions/callback-auto-dialer-campaign-execution.md) | `POST /auto_dialer_campaigns/{auto_dialer_campaign_id}/execution_callback` | [docs](https://api.seasalt.ai/seax/) |
| [Callback Auto Dialer Campaign Gather](actions/callback-auto-dialer-campaign-gather.md) | `POST /auto_dialer_campaigns/{auto_dialer_campaign_id}/gather_callback` | [docs](https://api.seasalt.ai/seax/) |
| [Create API Key](actions/create-api-key.md) | `POST /api_keys` | [docs](https://api.seasalt.ai/seax/) |
| [Create Auto Dialer Campaign](actions/create-auto-dialer-campaign.md) | `POST /auto_dialer_campaigns` | [docs](https://api.seasalt.ai/seax/) |
| [Create Auto Dialer Campaign Webhook](actions/create-auto-dialer-campaign-webhook.md) | `POST /auto_dialer_campaigns/{auto_dialer_campaign_id}/webhooks` | [docs](https://api.seasalt.ai/seax/) |
| [Create Campaign](actions/create-campaign.md) | `POST /campaigns` | [docs](https://api.seasalt.ai/seax/) |
| [Create Campaign Webhook](actions/create-campaign-webhook.md) | `POST /campaigns/{campaign_id}/webhooks` | [docs](https://api.seasalt.ai/seax/) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://api.seasalt.ai/seax/) |
| [Create Contact Label](actions/create-contact-label.md) | `POST /contact_labels` | [docs](https://api.seasalt.ai/seax/) |
| [Create General Call Campaign](actions/create-general-call-campaign.md) | `POST /general_campaigns/call` | [docs](https://api.seasalt.ai/seax/) |
| [Create General SMS Campaign](actions/create-general-sms-campaign.md) | `POST /general_campaigns/sms` | [docs](https://api.seasalt.ai/seax/) |
| [Create General WABP Campaign](actions/create-general-wabp-campaign.md) | `POST /general_campaigns/wabp` | [docs](https://api.seasalt.ai/seax/) |
| [Create Highly Structured Message Campaign](actions/create-highly-structured-message-campaign.md) | `POST /highly_structured_message/campaign` | [docs](https://api.seasalt.ai/seax/) |
| [Create Phone](actions/create-phone.md) | `POST /phones` | [docs](https://api.seasalt.ai/seax/) |
| [Delete API Key](actions/delete-api-key.md) | `DELETE /api_keys/{api_key_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Delete Auto Dialer Campaign](actions/delete-auto-dialer-campaign.md) | `DELETE /auto_dialer_campaigns/{auto_dialer_campaign_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Delete Campaign](actions/delete-campaign.md) | `DELETE /campaigns/{campaign_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/{contact_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Delete Contact Label](actions/delete-contact-label.md) | `DELETE /contact_labels/{contact_label_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Delete Instagram Integration](actions/delete-instagram-integration.md) | `DELETE /instagram/phone/{phone_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Delete LINE Official Integration](actions/delete-line-official-integration.md) | `DELETE /line_official/phone/{phone_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Delete Messenger Integration](actions/delete-messenger-integration.md) | `DELETE /messenger/phone/{phone_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Delete Phone](actions/delete-phone.md) | `DELETE /phones/{phone_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Delete WhatsApp Business Platform Account](actions/delete-whatsapp-business-platform-account.md) | `DELETE /whatsapp_business_platform/{service_provider_account_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Download Auto Dialer Campaign Contact Template](actions/download-auto-dialer-campaign-contact-template.md) | `GET /auto_dialer_campaigns/{auto_dialer_campaign_id}/download_contact_template` | [docs](https://api.seasalt.ai/seax/) |
| [Download Auto Dialer Campaign Logs](actions/download-auto-dialer-campaign-logs.md) | `GET /auto_dialer_campaigns/{auto_dialer_campaign_id}/download_logs` | [docs](https://api.seasalt.ai/seax/) |
| [Download Campaign Contact Template](actions/download-campaign-contact-template.md) | `GET /campaigns/{campaign_id}/download_contact_template` | [docs](https://api.seasalt.ai/seax/) |
| [Download Campaign Logs](actions/download-campaign-logs.md) | `GET /campaigns/{campaign_id}/download_logs` | [docs](https://api.seasalt.ai/seax/) |
| [Dry Run Auto Dialer Campaign](actions/dry-run-auto-dialer-campaign.md) | `POST /auto_dialer_campaigns/dry_run` | [docs](https://api.seasalt.ai/seax/) |
| [Get Auto Dialer Campaign](actions/get-auto-dialer-campaign.md) | `GET /auto_dialer_campaigns/{auto_dialer_campaign_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Get Auto Dialer Campaign Results](actions/get-auto-dialer-campaign-results.md) | `GET /auto_dialer_campaigns/{auto_dialer_campaign_id}/results` | [docs](https://api.seasalt.ai/seax/) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/{campaign_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Get Conversation](actions/get-conversation.md) | `GET /conversations/{conversation_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Get Instagram Integration](actions/get-instagram-integration.md) | `GET /instagram/phone/{phone_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Get Job](actions/get-job.md) | `GET /jobs/{job_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Get LINE Official Integration](actions/get-line-official-integration.md) | `GET /line_official/phone/{phone_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Get Messaging Service](actions/get-messaging-service.md) | `GET /messaging_services/{messaging_service_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Get Messenger Integration](actions/get-messenger-integration.md) | `GET /messenger/phone/{phone_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Import Contacts](actions/import-contacts.md) | `POST /import_contacts` | [docs](https://api.seasalt.ai/seax/) |
| [List AI Agents](actions/list-ai-agents.md) | `GET /ai_agents` | [docs](https://api.seasalt.ai/seax/) |
| [List API Keys](actions/list-api-keys.md) | `GET /api_keys` | [docs](https://api.seasalt.ai/seax/) |
| [List Auto Dialer Campaign Jobs](actions/list-auto-dialer-campaign-jobs.md) | `GET /auto_dialer_campaigns/{auto_dialer_campaign_id}/jobs` | [docs](https://api.seasalt.ai/seax/) |
| [List Auto Dialer Campaign Logs](actions/list-auto-dialer-campaign-logs.md) | `GET /auto_dialer_campaigns/{auto_dialer_campaign_id}/logs` | [docs](https://api.seasalt.ai/seax/) |
| [List Auto Dialer Campaigns](actions/list-auto-dialer-campaigns.md) | `GET /auto_dialer_campaigns` | [docs](https://api.seasalt.ai/seax/) |
| [List Campaign Logs](actions/list-campaign-logs.md) | `GET /campaigns/{campaign_id}/logs` | [docs](https://api.seasalt.ai/seax/) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://api.seasalt.ai/seax/) |
| [List Contact Labels](actions/list-contact-labels.md) | `GET /contact_labels` | [docs](https://api.seasalt.ai/seax/) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://api.seasalt.ai/seax/) |
| [List Conversation Messages](actions/list-conversation-messages.md) | `GET /conversations/{conversation_id}/messages` | [docs](https://api.seasalt.ai/seax/) |
| [List Conversations](actions/list-conversations.md) | `GET /conversations` | [docs](https://api.seasalt.ai/seax/) |
| [List Jobs](actions/list-jobs.md) | `GET /jobs` | [docs](https://api.seasalt.ai/seax/) |
| [List Messages](actions/list-messages.md) | `GET /message` | [docs](https://api.seasalt.ai/seax/) |
| [List Messaging Services](actions/list-messaging-services.md) | `GET /messaging_services` | [docs](https://api.seasalt.ai/seax/) |
| [List Phone Revisions](actions/list-phone-revisions.md) | `GET /phones/{phone_id}/revisions` | [docs](https://api.seasalt.ai/seax/) |
| [List Phones](actions/list-phones.md) | `GET /phones` | [docs](https://api.seasalt.ai/seax/) |
| [List User Activity Logs](actions/list-user-activity-logs.md) | `GET /user_activity_logs` | [docs](https://api.seasalt.ai/seax/) |
| [List Voice Call Sessions](actions/list-voice-call-sessions.md) | `GET /voice_call_sessions` | [docs](https://api.seasalt.ai/seax/) |
| [List WhatsApp Business Platform Accounts](actions/list-whatsapp-business-platform-accounts.md) | `GET /whatsapp_business_platform` | [docs](https://api.seasalt.ai/seax/) |
| [List WhatsApp Business Platform Highly Structured Templates](actions/list-whatsapp-business-platform-highly-structured-templates.md) | `GET /whatsapp_business_platform_templates/{phone_number}` | [docs](https://api.seasalt.ai/seax/) |
| [List WhatsApp Business Platform Templates](actions/list-whatsapp-business-platform-templates.md) | `GET /whatsapp_business_platform/{service_provider_account_id}/templates` | [docs](https://api.seasalt.ai/seax/) |
| [Query Phone](actions/query-phone.md) | `POST /phones/query_phone` | [docs](https://api.seasalt.ai/seax/) |
| [Refresh Voice Call Session](actions/refresh-voice-call-session.md) | `POST /voice_call_sessions/{session_id}/refresh` | [docs](https://api.seasalt.ai/seax/) |
| [Reset API Keys](actions/reset-api-keys.md) | `POST /api_keys/reset` | [docs](https://api.seasalt.ai/seax/) |
| [Resync WhatsApp Business Platform Account](actions/resync-whatsapp-business-platform-account.md) | `POST /whatsapp_business_platform/{service_provider_account_id}/sync` | [docs](https://api.seasalt.ai/seax/) |
| [Send Highly Structured Message](actions/send-highly-structured-message.md) | `POST /highly_structured_message/message` | [docs](https://api.seasalt.ai/seax/) |
| [Send Message](actions/send-message.md) | `POST /send_message` | [docs](https://api.seasalt.ai/seax/) |
| [Send SMS Message](actions/send-sms-message.md) | `POST /messages/sms` | [docs](https://api.seasalt.ai/seax/) |
| [Send WABP Message](actions/send-wabp-message.md) | `POST /messages/wabp` | [docs](https://api.seasalt.ai/seax/) |
| [Send WABP Template Message](actions/send-wabp-template-message.md) | `POST /send_message/wabp_template_message` | [docs](https://api.seasalt.ai/seax/) |
| [Sync WhatsApp Business Platform By Code](actions/sync-whatsapp-business-platform-by-code.md) | `POST /whatsapp_business_platform` | [docs](https://api.seasalt.ai/seax/) |
| [Unset Phone Recipient](actions/unset-phone-recipient.md) | `POST /phones/{phone_id}/unset_recipient` | [docs](https://api.seasalt.ai/seax/) |
| [Unset Verified Caller](actions/unset-verified-caller.md) | `POST /phones/{phone_id}/unset` | [docs](https://api.seasalt.ai/seax/) |
| [Update API Key](actions/update-api-key.md) | `PATCH /api_keys/{api_key_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Update Auto Dialer Campaign](actions/update-auto-dialer-campaign.md) | `PATCH /auto_dialer_campaigns/{auto_dialer_campaign_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Update Campaign](actions/update-campaign.md) | `PATCH /campaigns/{campaign_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Update Contact](actions/update-contact.md) | `PATCH /contacts/{contact_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Update Contact Label](actions/update-contact-label.md) | `PATCH /contact_labels/{contact_label_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Update Conversation](actions/update-conversation.md) | `PATCH /conversations/{conversation_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Update Phone](actions/update-phone.md) | `PATCH /phones/{phone_id}` | [docs](https://api.seasalt.ai/seax/) |
| [Upsert Instagram Integration](actions/upsert-instagram-integration.md) | `PUT /instagram` | [docs](https://api.seasalt.ai/seax/) |
| [Upsert LINE Official Integration](actions/upsert-line-official-integration.md) | `PUT /line_official` | [docs](https://api.seasalt.ai/seax/) |
| [Upsert Messenger Integration](actions/upsert-messenger-integration.md) | `PUT /messenger` | [docs](https://api.seasalt.ai/seax/) |
| [Validate Auto Dialer Campaign](actions/validate-auto-dialer-campaign.md) | `POST /auto_dialer_campaigns/{auto_dialer_campaign_id}/validate` | [docs](https://api.seasalt.ai/seax/) |
| [Validate Auto Dialer Campaign Contact File](actions/validate-auto-dialer-campaign-contact-file.md) | `POST /auto_dialer_campaigns/{auto_dialer_campaign_id}/validate_contact_file` | [docs](https://api.seasalt.ai/seax/) |
| [Validate Campaign Contact File](actions/validate-campaign-contact-file.md) | `POST /campaigns/{campaign_id}/validate_contact_file` | [docs](https://api.seasalt.ai/seax/) |
