# Maildrip: Native API Reference

A consolidated summary of Maildrip's API configuration and 167 documented operations, with links to official documentation.

- **Official docs:** https://api.maildrip.io/docs/
- **OpenAPI specification:** https://challaris.github.io/maildrip-server/swagger.json
- **API base URL:** `https://api.maildrip.io`

## Authentication

### API Key

Connect Maildrip with an API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://maildrip.gitbook.io/documentation/developers/getting-started)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `limit` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (167 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add a contact](actions/add-a-contact.md) | `POST /api/v1/contacts` | [docs](https://api.maildrip.io/docs/) |
| [Add a new card for the user](actions/add-a-new-card-for-the-user.md) | `POST /api/v1/payment/stripe/customer/cards` | [docs](https://api.maildrip.io/docs/) |
| [Add a new sending node to a domain group](actions/add-a-new-sending-node-to-a-domain-group.md) | `POST /api/v1/mumara/sending-nodes` | [docs](https://api.maildrip.io/docs/) |
| [Add a new user to Mumara](actions/add-a-new-user-to-mumara.md) | `POST /api/v1/mumara/users` | [docs](https://api.maildrip.io/docs/) |
| [Add a user to the campaign](actions/add-a-user-to-the-campaign.md) | `POST /api/v1/campaigns/{campaign_id}/user` | [docs](https://api.maildrip.io/docs/) |
| [Add an email to a campaign](actions/add-an-email-to-a-campaign.md) | `POST /api/v1/campaigns/{campaignId}/addmail` | [docs](https://api.maildrip.io/docs/) |
| [Add contact to opt-in page's groups](actions/add-contact-to-opt-in-page-s-groups.md) | `POST /api/v1/opt-in-pages/{pageId}` | [docs](https://api.maildrip.io/docs/) |
| [Add contacts in bulk to a group](actions/add-contacts-in-bulk-to-a-group.md) | `POST /api/v1/contacts/bulk` | [docs](https://api.maildrip.io/docs/) |
| [Analyze email subject or body content and provide a performance report](actions/analyze-email-subject-or-body-content-and-provide-a-performance-report.md) | `POST /api/v1/ai-assistant/analyze` | [docs](https://api.maildrip.io/docs/) |
| [Atomically create a contact group and attach it to an opt-in page](actions/atomically-create-a-contact-group-and-attach-it-to-an-opt-in-page.md) | `POST /api/v1/opt-in-pages/{pageId}/groups` | [docs](https://api.maildrip.io/docs/) |
| [Atomically create a draft campaign + draft email for an opt-in page](actions/atomically-create-a-draft-campaign-draft-email-for-an-opt-in-page.md) | `POST /api/v1/opt-in-pages/{pageId}/quick-campaign` | [docs](https://api.maildrip.io/docs/) |
| [Authorize a transaction](actions/authorize-a-transaction.md) | `POST /api/v1/payment/paystack/transactions/authorize` | [docs](https://api.maildrip.io/docs/) |
| [Cancel a subscription](actions/cancel-a-subscription.md) | `GET /api/v1/payment/paystack/subscriptions/cancel` | [docs](https://api.maildrip.io/docs/) |
| [Cancel an active subscription for a user](actions/cancel-an-active-subscription-for-a-user.md) | `PATCH /api/v1/payment/stripe/subscription/cancel` | [docs](https://api.maildrip.io/docs/) |
| [Change user password](actions/change-user-password.md) | `PATCH /api/v1/users/change-password` | [docs](https://api.maildrip.io/docs/) |
| [Clone a public template or user-owned template](actions/clone-a-public-template-or-user-owned-template.md) | `POST /api/v1/templates/clone/{templateId}` | [docs](https://api.maildrip.io/docs/) |
| [Clone an instant email](actions/clone-an-instant-email.md) | `POST /api/v1/instant-emails/clone/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Create a new campaign](actions/create-a-new-campaign.md) | `POST /api/v1/campaigns` | [docs](https://api.maildrip.io/docs/) |
| [Create a new contacts group](actions/create-a-new-contacts-group.md) | `POST /api/v1/contacts/groups` | [docs](https://api.maildrip.io/docs/) |
| [Create a new opt-in page](actions/create-a-new-opt-in-page.md) | `POST /api/v1/opt-in-pages` | [docs](https://api.maildrip.io/docs/) |
| [Create a new subscription for a user](actions/create-a-new-subscription-for-a-user.md) | `POST /api/v1/payment/stripe/subscription/create` | [docs](https://api.maildrip.io/docs/) |
| [Create a pay-as-you-go transaction](actions/create-a-pay-as-you-go-transaction.md) | `POST /api/v1/payment/paystack/transactions` | [docs](https://api.maildrip.io/docs/) |
| [Create a payment intent](actions/create-a-payment-intent.md) | `POST /api/v1/payment/stripe/payment-intent/create` | [docs](https://api.maildrip.io/docs/) |
| [Create a subscription](actions/create-a-subscription.md) | `POST /api/v1/payment/paystack/subscriptions` | [docs](https://api.maildrip.io/docs/) |
| [Create a top-up transaction](actions/create-a-top-up-transaction.md) | `POST /api/v1/payment/paystack/transactions/topup` | [docs](https://api.maildrip.io/docs/) |
| [Create an instant email](actions/create-an-instant-email.md) | `POST /api/v1/instant-emails` | [docs](https://api.maildrip.io/docs/) |
| [Deactivate the account of the logged-in user](actions/deactivate-the-account-of-the-logged-in-user.md) | `PATCH /api/v1/users/deactivate-account` | [docs](https://api.maildrip.io/docs/) |
| [Delete a campaign variable](actions/delete-a-campaign-variable.md) | `DELETE /api/v1/campaigns/{campaign_id}/variables` | [docs](https://api.maildrip.io/docs/) |
| [Delete a card](actions/delete-a-card.md) | `DELETE /api/v1/payment/paystack/cards/{authorization}` | [docs](https://api.maildrip.io/docs/) |
| [Delete a contact from a specific group](actions/delete-a-contact-from-a-specific-group.md) | `DELETE /api/v1/contacts/group/{group_id}` | [docs](https://api.maildrip.io/docs/) |
| [Delete a contact group](actions/delete-a-contact-group.md) | `DELETE /api/v1/contacts/groups/{groupId}` | [docs](https://api.maildrip.io/docs/) |
| [Delete a landing page by ID](actions/delete-a-landing-page-by-id.md) | `DELETE /api/v1/landing-page/{pageId}` | [docs](https://api.maildrip.io/docs/) |
| [Delete a sending domain from Mumara](actions/delete-a-sending-domain-from-mumara.md) | `DELETE /api/v1/mumara/sending-domains/{id}` | [docs](https://api.maildrip.io/docs/) |
| [Delete a user from Mumara](actions/delete-a-user-from-mumara.md) | `DELETE /api/v1/mumara/users/delete/{type}` | [docs](https://api.maildrip.io/docs/) |
| [Delete a user's card](actions/delete-a-user-s-card.md) | `DELETE /api/v1/payment/stripe/customer/cards/{id}` | [docs](https://api.maildrip.io/docs/) |
| [Delete an attachment from a email](actions/delete-an-attachment-from-a-email.md) | `DELETE /api/v1/attachments/` | [docs](https://api.maildrip.io/docs/) |
| [Delete an email from a campaign](actions/delete-an-email-from-a-campaign.md) | `DELETE /api/v1/campaigns/{campaignId}/{campaignEmailId}` | [docs](https://api.maildrip.io/docs/) |
| [Delete an opt-in page by ID](actions/delete-an-opt-in-page-by-id.md) | `DELETE /api/v1/opt-in-pages/{pageId}` | [docs](https://api.maildrip.io/docs/) |
| [Delete campaign](actions/delete-campaign.md) | `DELETE /api/v1/campaigns/{campaignId}` | [docs](https://api.maildrip.io/docs/) |
| [Delete instant email by ID](actions/delete-instant-email-by-id.md) | `DELETE /api/v1/instant-emails/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Delete user from campaign](actions/delete-user-from-campaign.md) | `DELETE /api/v1/campaigns/{campaign_id}/{recipient_id}/user` | [docs](https://api.maildrip.io/docs/) |
| [Duplicate an existing campaign](actions/duplicate-an-existing-campaign.md) | `POST /api/v1/campaigns/{campaignId}/duplicate` | [docs](https://api.maildrip.io/docs/) |
| [Edit a contact](actions/edit-a-contact.md) | `POST /api/v1/contacts/{contact_id}` | [docs](https://api.maildrip.io/docs/) |
| [Edit campaign variables](actions/edit-campaign-variables.md) | `PUT /api/v1/campaigns/{campaign_id}/variables` | [docs](https://api.maildrip.io/docs/) |
| [Edit instant email](actions/edit-instant-email.md) | `PATCH /api/v1/instant-emails/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Execute an MCP tool](actions/execute-an-mcp-tool.md) | `POST /api/v1/mcp/tools/call` | [docs](https://api.maildrip.io/docs/) |
| [Fix and optimize manual email content using AI and analysis report (paid users only)](actions/fix-and-optimize-manual-email-content-using-ai-and-analysis-report-paid-users-only.md) | `POST /api/v1/ai-assistant/fix` | [docs](https://api.maildrip.io/docs/) |
| [Generate a new AI email template from a natural language prompt](actions/generate-a-new-ai-email-template-from-a-natural-language-prompt.md) | `POST /api/v1/ai-template/generate` | [docs](https://api.maildrip.io/docs/) |
| [Generate email subject or body content using AI](actions/generate-email-subject-or-body-content-using-ai.md) | `POST /api/v1/ai-assistant/generate` | [docs](https://api.maildrip.io/docs/) |
| [Get a published opt-in page by ID (public, no auth required)](actions/get-a-published-opt-in-page-by-id-public-no-auth-required.md) | `GET /api/v1/public/opt-in-pages/{pageId}` | [docs](https://api.maildrip.io/docs/) |
| [Get account health status](actions/get-account-health-status.md) | `GET /api/v1/fraud/health` | [docs](https://api.maildrip.io/docs/) |
| [Get AI assistant capabilities](actions/get-ai-assistant-capabilities.md) | `GET /api/v1/chat/capabilities` | [docs](https://api.maildrip.io/docs/) |
| [Get all active promos](actions/get-all-active-promos.md) | `GET /api/v1/promo/active` | [docs](https://api.maildrip.io/docs/) |
| [Get all available plans](actions/get-all-available-plans.md) | `GET /api/v1/plans` | [docs](https://api.maildrip.io/docs/) |
| [Get all available subscription plans with IDs](actions/get-all-available-subscription-plans-with-ids.md) | `GET /api/v1/promo/plans` | [docs](https://api.maildrip.io/docs/) |
| [Get all contact groups](actions/get-all-contact-groups.md) | `GET /api/v1/contacts/groups` | [docs](https://api.maildrip.io/docs/) |
| [Get all distinct metadata attribute keys for user's contacts](actions/get-all-distinct-metadata-attribute-keys-for-user-s-contacts.md) | `GET /api/v1/contacts/attribute-keys` | [docs](https://api.maildrip.io/docs/) |
| [Get an email by ID for a specific campaign](actions/get-an-email-by-id-for-a-specific-campaign.md) | `GET /api/v1/campaigns/{campaignId}/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Get an opt-in page by ID](actions/get-an-opt-in-page-by-id.md) | `GET /api/v1/opt-in-pages/{pageId}` | [docs](https://api.maildrip.io/docs/) |
| [Get API credentials](actions/get-api-credentials.md) | `GET /api/v1/users/credentials` | [docs](https://api.maildrip.io/docs/) |
| [Get campaign variables](actions/get-campaign-variables.md) | `GET /api/v1/campaigns/{campaign_id}/variables` | [docs](https://api.maildrip.io/docs/) |
| [Get contact count by attribute filters](actions/get-contact-count-by-attribute-filters.md) | `GET /api/v1/contacts/count` | [docs](https://api.maildrip.io/docs/) |
| [Get contact counts for an opt-in page's linked groups](actions/get-contact-counts-for-an-opt-in-page-s-linked-groups.md) | `GET /api/v1/opt-in-pages/{pageId}/stats` | [docs](https://api.maildrip.io/docs/) |
| [Get contacts in a specific group or all contacts](actions/get-contacts-in-a-specific-group-or-all-contacts.md) | `GET /api/v1/contacts/group` | [docs](https://api.maildrip.io/docs/) |
| [Get details about a specific tool](actions/get-details-about-a-specific-tool.md) | `GET /api/v1/mcp/tools/{toolName}` | [docs](https://api.maildrip.io/docs/) |
| [Get details of a specific sending node](actions/get-details-of-a-specific-sending-node.md) | `GET /api/v1/mumara/sending-nodes/{nodeId}` | [docs](https://api.maildrip.io/docs/) |
| [Get emails for a specific recipient in a campaign](actions/get-emails-for-a-specific-recipient-in-a-campaign.md) | `POST /api/v1/campaigns/{campaignId}/recipient-emails` | [docs](https://api.maildrip.io/docs/) |
| [Get instant email by ID](actions/get-instant-email-by-id.md) | `GET /api/v1/instant-emails/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Get landing page by ID](actions/get-landing-page-by-id.md) | `GET /api/v1/landing-page/{pageId}` | [docs](https://api.maildrip.io/docs/) |
| [Get landing page details for a campaign](actions/get-landing-page-details-for-a-campaign.md) | `GET /api/v1/campaigns/{campaignId}/landing-page` | [docs](https://api.maildrip.io/docs/) |
| [Get landing pages](actions/get-landing-pages.md) | `GET /api/v1/get-all-pages` | [docs](https://api.maildrip.io/docs/) |
| [Get MCP server information and capabilities](actions/get-mcp-server-information-and-capabilities.md) | `GET /api/v1/mcp` | [docs](https://api.maildrip.io/docs/) |
| [Get opt-in pages](actions/get-opt-in-pages.md) | `GET /api/v1/opt-in-pages` | [docs](https://api.maildrip.io/docs/) |
| [Get page, setup, checklist, and stats in a single call](actions/get-page-setup-checklist-and-stats-in-a-single-call.md) | `GET /api/v1/opt-in-pages/{pageId}/editor-summary` | [docs](https://api.maildrip.io/docs/) |
| [Get pre-publish checklist for an opt-in page](actions/get-pre-publish-checklist-for-an-opt-in-page.md) | `GET /api/v1/opt-in-pages/{pageId}/pre-publish-check` | [docs](https://api.maildrip.io/docs/) |
| [Get promo pricing for a plan (public - all users see promo prices)](actions/get-promo-pricing-for-a-plan-public-all-users-see-promo-prices.md) | `GET /api/v1/promo/pricing` | [docs](https://api.maildrip.io/docs/) |
| [Get public templates with filtering and sorting](actions/get-public-templates-with-filtering-and-sorting.md) | `GET /api/v1/templates/public` | [docs](https://api.maildrip.io/docs/) |
| [Get segment statistics](actions/get-segment-statistics.md) | `GET /api/v1/segments/{id}/stats` | [docs](https://api.maildrip.io/docs/) |
| [Get sending domains from Mumara](actions/get-sending-domains-from-mumara.md) | `GET /api/v1/mumara/sending-domains` | [docs](https://api.maildrip.io/docs/) |
| [Get suggested prompts for the chat interface](actions/get-suggested-prompts-for-the-chat-interface.md) | `GET /api/v1/chat/suggestions` | [docs](https://api.maildrip.io/docs/) |
| [Get top-up rate](actions/get-top-up-rate.md) | `GET /api/v1/payment/paystack/transactions/topup` | [docs](https://api.maildrip.io/docs/) |
| [Get updated pay-as-you-go rate](actions/get-updated-pay-as-you-go-rate.md) | `GET /api/v1/payment/paystack/transactions` | [docs](https://api.maildrip.io/docs/) |
| [Get user details](actions/get-user-details.md) | `GET /api/v1/users/me` | [docs](https://api.maildrip.io/docs/) |
| [Get user's saved cards from Paystack](actions/get-user-s-saved-cards-from-paystack.md) | `GET /api/v1/payment/paystack/cards` | [docs](https://api.maildrip.io/docs/) |
| [Get user transactions](actions/get-user-transactions.md) | `GET /api/v1/payment/transactions` | [docs](https://api.maildrip.io/docs/) |
| [Get UTM attribution breakdown for an opt-in page's signups](actions/get-utm-attribution-breakdown-for-an-opt-in-page-s-signups.md) | `GET /api/v1/opt-in-pages/{pageId}/stats/utm` | [docs](https://api.maildrip.io/docs/) |
| [Google OAuth signup or login](actions/google-oauth-signup-or-login.md) | `POST /api/v1/oauth/google` | [docs](https://api.maildrip.io/docs/) |
| [Identify a contact and sync attributes from your app](actions/identify-a-contact-and-sync-attributes-from-your-app.md) | `POST /api/v1/identify` | [docs](https://api.maildrip.io/docs/) |
| [Import contact groups to an instant email](actions/import-contact-groups-to-an-instant-email.md) | `POST /api/v1/instant-emails/save-groups/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Import contacts from groups to a campaign](actions/import-contacts-from-groups-to-a-campaign.md) | `POST /api/v1/campaigns/{campaign_id}/contacts` | [docs](https://api.maildrip.io/docs/) |
| [Import contacts to a campaign](actions/import-contacts-to-a-campaign.md) | `POST /api/v1/{campaignId}/contacts/import` | [docs](https://api.maildrip.io/docs/) |
| [Import CSV contacts to an instant email](actions/import-csv-contacts-to-an-instant-email.md) | `POST /api/v1/instant-emails/upload/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Iteratively improve an existing AI-generated email template](actions/iteratively-improve-an-existing-ai-generated-email-template.md) | `POST /api/v1/ai-template/refine/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Join a campaign as a guest](actions/join-a-campaign-as-a-guest.md) | `POST /api/v1/campaigns/{campaign_id}/join-as-guest` | [docs](https://api.maildrip.io/docs/) |
| [List all available MCP tools](actions/list-all-available-mcp-tools.md) | `GET /api/v1/mcp/tools` | [docs](https://api.maildrip.io/docs/) |
| [Login to the application](actions/login-to-the-application.md) | `POST /api/v1/users/login` | [docs](https://api.maildrip.io/docs/) |
| [Manually regenerate AI review (costs 5 AI credits)](actions/manually-regenerate-ai-review-costs5-ai-credits.md) | `POST /api/v1/templates/{templateId}/review` | [docs](https://api.maildrip.io/docs/) |
| [Manually trigger segment re-evaluation](actions/manually-trigger-segment-re-evaluation.md) | `POST /api/v1/contacts/groups/{id}/re-evaluate` | [docs](https://api.maildrip.io/docs/) |
| [Modify contacts by adding them to specified groups and optionally to a campaign.](actions/modify-contacts-by-adding-them-to-specified-groups-and-optionally-to-a-campaign.md) | `POST /api/v1/contacts/modify/{groupId}` | [docs](https://api.maildrip.io/docs/) |
| [Partially update an opt-in page (e.g. rename)](actions/partially-update-an-opt-in-page-eg-rename.md) | `PATCH /api/v1/opt-in-pages/{pageId}` | [docs](https://api.maildrip.io/docs/) |
| [Perform a detailed analysis of email content and provide manual recommendations (paid users only)](actions/perform-a-detailed-analysis-of-email-content-and-provide-manual-recommendations-paid-users-only.md) | `POST /api/v1/ai-assistant/detailed-analysis` | [docs](https://api.maildrip.io/docs/) |
| [Platform-internal identify — sync dashboard user attributes](actions/platform-internal-identify-sync-dashboard-user-attributes.md) | `POST /api/v1/platform/identify` | [docs](https://api.maildrip.io/docs/) |
| [Preview contacts in segment for campaign](actions/preview-contacts-in-segment-for-campaign.md) | `GET /api/v1/campaigns/{campaignId}/segment/preview` | [docs](https://api.maildrip.io/docs/) |
| [Preview segment membership without saving](actions/preview-segment-membership-without-saving.md) | `POST /api/v1/segments/preview` | [docs](https://api.maildrip.io/docs/) |
| [Publish an opt-in page](actions/publish-an-opt-in-page.md) | `PUT /api/v1/opt-in-pages/{pageId}/publish` | [docs](https://api.maildrip.io/docs/) |
| [Reactivate a canceled subscription for a user](actions/reactivate-a-canceled-subscription-for-a-user.md) | `PATCH /api/v1/payment/stripe/subscription/reactivate` | [docs](https://api.maildrip.io/docs/) |
| [Reactivate a deactivated account](actions/reactivate-a-deactivated-account.md) | `POST /api/v1/users/reactivate-account` | [docs](https://api.maildrip.io/docs/) |
| [Receive webhook from Mumara](actions/receive-webhook-from-mumara.md) | `POST /api/v1/mumara/webhook` | [docs](https://api.maildrip.io/docs/) |
| [Record promo usage when user subscribes](actions/record-promo-usage-when-user-subscribes.md) | `POST /api/v1/promo/record-usage` | [docs](https://api.maildrip.io/docs/) |
| [Register a new user](actions/register-a-new-user.md) | `POST /api/v1/users/register` | [docs](https://api.maildrip.io/docs/) |
| [Remove contacts from a group or delete them entirely (asynchronous).](actions/remove-contacts-from-a-group-or-delete-them-entirely-asynchronous.md) | `PUT /api/v1/contacts/delete` | [docs](https://api.maildrip.io/docs/) |
| [Rename a user-owned template](actions/rename-a-user-owned-template.md) | `PATCH /api/v1/templates/my-templates/{templateId}` | [docs](https://api.maildrip.io/docs/) |
| [Reorder emails in a campaign](actions/reorder-emails-in-a-campaign.md) | `POST /api/v1/campaigns/{campaignId}/reorder` | [docs](https://api.maildrip.io/docs/) |
| [Resend verification email](actions/resend-verification-email.md) | `POST /api/v1/users/resend-verification-link` | [docs](https://api.maildrip.io/docs/) |
| [Reset password using the reset password hash](actions/reset-password-using-the-reset-password-hash.md) | `POST /api/v1/users/reset-password` | [docs](https://api.maildrip.io/docs/) |
| [Restore draft email to drafts](actions/restore-draft-email-to-drafts.md) | `PATCH /api/v1/campaigns/{campaignId}/{emailId}/restore-mail-to-draft` | [docs](https://api.maildrip.io/docs/) |
| [Restore draft email to editing](actions/restore-draft-email-to-editing.md) | `GET /api/v1/campaigns/{campaignId}/{emailId}/restore-mail-to-editing` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve a campaign by ID](actions/retrieve-a-campaign-by-id.md) | `GET /api/v1/campaigns/{campaign_id}` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve active emails of a campaign](actions/retrieve-active-emails-of-a-campaign.md) | `GET /api/v1/campaigns/{campaign_id}/active-mails` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve campaigns](actions/retrieve-campaigns.md) | `GET /api/v1/campaigns` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve data of a campaign](actions/retrieve-data-of-a-campaign.md) | `GET /api/v1/campaigns/{campaign_id}/get-data` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve deleted emails of a campaign](actions/retrieve-deleted-emails-of-a-campaign.md) | `GET /api/v1/campaigns/{campaign_id}/deleted-mails` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve draft emails of a campaign](actions/retrieve-draft-emails-of-a-campaign.md) | `GET /api/v1/campaigns/{campaign_id}/draft-mails` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve instant emails](actions/retrieve-instant-emails.md) | `GET /api/v1/instant-emails` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve sending nodes from Mumara](actions/retrieve-sending-nodes-from-mumara.md) | `GET /api/v1/mumara/sending-nodes` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve the user's saved cards](actions/retrieve-the-user-s-saved-cards.md) | `GET /api/v1/payment/stripe/customer/cards` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve User Templates](actions/retrieve-user-templates.md) | `GET /api/v1/template` | [docs](https://api.maildrip.io/docs/) |
| [Retrieve users associated with a campaign](actions/retrieve-users-associated-with-a-campaign.md) | `GET /api/v1/campaigns/{campaign_id}/user` | [docs](https://api.maildrip.io/docs/) |
| [Save email as draft](actions/save-email-as-draft.md) | `POST /api/v1/instant-emails/save-as-draft/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Save email draft for a campaign](actions/save-email-draft-for-a-campaign.md) | `POST /api/v1/campaigns/{campaign_id}/save-draft` | [docs](https://api.maildrip.io/docs/) |
| [Send a chat message to the AI assistant](actions/send-a-chat-message-to-the-ai-assistant.md) | `POST /api/v1/chat` | [docs](https://api.maildrip.io/docs/) |
| [Send a test mail for an instant email](actions/send-a-test-mail-for-an-instant-email.md) | `POST /api/v1/instant-emails/send-test-mail` | [docs](https://api.maildrip.io/docs/) |
| [Send a test mail for the campaign](actions/send-a-test-mail-for-the-campaign.md) | `POST /api/v1/campaigns/{campaignId}/send-test-mail` | [docs](https://api.maildrip.io/docs/) |
| [Send a transactional email using a template](actions/send-a-transactional-email-using-a-template.md) | `POST /api/v1/emails/transaction/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Send a transactional email with raw data](actions/send-a-transactional-email-with-raw-data.md) | `POST /api/v1/emails/transaction` | [docs](https://api.maildrip.io/docs/) |
| [Send email to trash](actions/send-email-to-trash.md) | `PATCH /api/v1/campaigns/{campaign_id}/{campaign_email_id}/send-mail-to-trash` | [docs](https://api.maildrip.io/docs/) |
| [Send email via Mumara](actions/send-email-via-mumara.md) | `POST /api/v1/mumara/send-email` | [docs](https://api.maildrip.io/docs/) |
| [Send onboarding test mail using dedicated test domains](actions/send-onboarding-test-mail-using-dedicated-test-domains.md) | `POST /api/v1/onboarding/test-email` | [docs](https://api.maildrip.io/docs/) |
| [Send reset password email](actions/send-reset-password-email.md) | `POST /api/v1/users/forget-password` | [docs](https://api.maildrip.io/docs/) |
| [Set a card as default](actions/set-a-card-as-default.md) | `PATCH /api/v1/payment/paystack/cards/{authorization}` | [docs](https://api.maildrip.io/docs/) |
| [Set a user's card as the default card](actions/set-a-user-s-card-as-the-default-card.md) | `PATCH /api/v1/payment/stripe/customer/cards` | [docs](https://api.maildrip.io/docs/) |
| [Set campaign to target a dynamic segment](actions/set-campaign-to-target-a-dynamic-segment.md) | `POST /api/v1/campaigns/{campaignId}/segment` | [docs](https://api.maildrip.io/docs/) |
| [Submit an appeal for account blocking](actions/submit-an-appeal-for-account-blocking.md) | `POST /api/v1/fraud/appeal` | [docs](https://api.maildrip.io/docs/) |
| [Toggle template public/private (triggers AI review on first publish)](actions/toggle-template-public-private-triggers-ai-review-on-first-publish.md) | `PATCH /api/v1/templates/{templateId}/visibility` | [docs](https://api.maildrip.io/docs/) |
| [Top up subscription wallet](actions/top-up-subscription-wallet.md) | `POST /api/v1/payment/stripe/topup` | [docs](https://api.maildrip.io/docs/) |
| [Unpublish an opt-in page](actions/unpublish-an-opt-in-page.md) | `PUT /api/v1/opt-in-pages/{pageId}/unpublish` | [docs](https://api.maildrip.io/docs/) |
| [Update a user in Mumara](actions/update-a-user-in-mumara.md) | `PUT /api/v1/mumara/users/update` | [docs](https://api.maildrip.io/docs/) |
| [Update a user's subscription plan](actions/update-a-user-s-subscription-plan.md) | `POST /api/v1/payment/stripe/subscription/update` | [docs](https://api.maildrip.io/docs/) |
| [Update account settings for the logged-in user](actions/update-account-settings-for-the-logged-in-user.md) | `PATCH /api/v1/users/account-settings` | [docs](https://api.maildrip.io/docs/) |
| [Update campaign interval](actions/update-campaign-interval.md) | `POST /api/v1/campaigns/{campaign_id}/interval` | [docs](https://api.maildrip.io/docs/) |
| [Update campaign status](actions/update-campaign-status.md) | `PATCH /api/v1/campaigns/{campaign_id}/status` | [docs](https://api.maildrip.io/docs/) |
| [Update contact group description](actions/update-contact-group-description.md) | `PATCH /api/v1/contacts/groups/{groupId}` | [docs](https://api.maildrip.io/docs/) |
| [Update email configuration for a campaign](actions/update-email-configuration-for-a-campaign.md) | `POST /api/v1/campaigns/{campaign_id}/email-configuration` | [docs](https://api.maildrip.io/docs/) |
| [Update email content for a campaign](actions/update-email-content-for-a-campaign.md) | `PATCH /api/v1/campaigns/{campaignId}/{emailId}` | [docs](https://api.maildrip.io/docs/) |
| [Update email settings for the logged-in user](actions/update-email-settings-for-the-logged-in-user.md) | `PATCH /api/v1/users/email-settings` | [docs](https://api.maildrip.io/docs/) |
| [Update landing page details for a campaign](actions/update-landing-page-details-for-a-campaign.md) | `PUT /api/v1/campaigns/{campaignId}/landing-page` | [docs](https://api.maildrip.io/docs/) |
| [Update metadata attributes for multiple contacts](actions/update-metadata-attributes-for-multiple-contacts.md) | `PUT /api/v1/contacts/bulk-attributes` | [docs](https://api.maildrip.io/docs/) |
| [Update sending node status](actions/update-sending-node-status.md) | `PATCH /api/v1/mumara/sending-nodes/{nodeId}/status` | [docs](https://api.maildrip.io/docs/) |
| [Update subscription plan](actions/update-subscription-plan.md) | `POST /api/v1/payment/paystack/subscriptions/update` | [docs](https://api.maildrip.io/docs/) |
| [Update the low credit limit for email credits](actions/update-the-low-credit-limit-for-email-credits.md) | `POST /api/v1/users/email-credits` | [docs](https://api.maildrip.io/docs/) |
| [Upload attachment To An Email](actions/upload-attachment-to-an-email.md) | `POST /api/v1/attachments/{email_id}` | [docs](https://api.maildrip.io/docs/) |
| [Upload image for an opt-in page](actions/upload-image-for-an-opt-in-page.md) | `POST /api/v1/opt-in-pages/image-upload` | [docs](https://api.maildrip.io/docs/) |
| [Upload profile photo for the user](actions/upload-profile-photo-for-the-user.md) | `POST /api/v1/users/upload-photo` | [docs](https://api.maildrip.io/docs/) |
| [Validate a payment intent](actions/validate-a-payment-intent.md) | `POST /api/v1/payment/stripe/payment-intent/validate` | [docs](https://api.maildrip.io/docs/) |
| [Verify a Paystack transaction](actions/verify-a-paystack-transaction.md) | `GET /api/v1/payment/paystack/transactions/verify` | [docs](https://api.maildrip.io/docs/) |
| [Verify domain DNS records](actions/verify-domain-dns-records.md) | `POST /api/v1/mumara/sending-domains/{domainId}/verify` | [docs](https://api.maildrip.io/docs/) |
| [Verify the setup health of an opt-in page](actions/verify-the-setup-health-of-an-opt-in-page.md) | `GET /api/v1/opt-in-pages/{pageId}/verify-setup` | [docs](https://api.maildrip.io/docs/) |
