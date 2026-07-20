# <img src="https://images.mindcloud.co/apps/icons/maildrip-logo_1775510620515.jpeg" alt="Maildrip logo" width="28" height="28"> Maildrip: Universal API

Create campaigns, manage contacts, and automate email marketing

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/maildrip/latest
- **Category:** Marketing
- **Actions:** 167
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://maildrip.io
- **Vendor API docs:** https://api.maildrip.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get user details](actions/get-user-details.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/maildrip/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (167)

### Aiassistant

| Action | Method | Description |
| --- | --- | --- |
| [Analyze email subject or body content and provide a performance report](actions/analyze-email-subject-or-body-content-and-provide-a-performance-report.md) | GET |  |
| [Fix and optimize manual email content using AI and analysis report (paid users only)](actions/fix-and-optimize-manual-email-content-using-ai-and-analysis-report-paid-users-only.md) | PUT |  |
| [Generate email subject or body content using AI](actions/generate-email-subject-or-body-content-using-ai.md) | POST |  |
| [Perform a detailed analysis of email content and provide manual recommendations (paid users only)](actions/perform-a-detailed-analysis-of-email-content-and-provide-manual-recommendations-paid-users-only.md) | POST |  |

### Aitemplate

| Action | Method | Description |
| --- | --- | --- |
| [Generate a new AI email template from a natural language prompt](actions/generate-a-new-ai-email-template-from-a-natural-language-prompt.md) | POST |  |
| [Iteratively improve an existing AI-generated email template](actions/iteratively-improve-an-existing-ai-generated-email-template.md) | POST |  |

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [Delete an attachment from a email](actions/delete-an-attachment-from-a-email.md) | DELETE |  |
| [Upload attachment To An Email](actions/upload-attachment-to-an-email.md) | POST |  |

### Campaign

| Action | Method | Description |
| --- | --- | --- |
| [Add a user to the campaign](actions/add-a-user-to-the-campaign.md) | POST |  |
| [Add an email to a campaign](actions/add-an-email-to-a-campaign.md) | POST |  |
| [Create a new campaign](actions/create-a-new-campaign.md) | POST |  |
| [Delete a campaign variable](actions/delete-a-campaign-variable.md) | DELETE |  |
| [Delete an email from a campaign](actions/delete-an-email-from-a-campaign.md) | DELETE |  |
| [Delete campaign](actions/delete-campaign.md) | DELETE |  |
| [Delete user from campaign](actions/delete-user-from-campaign.md) | DELETE |  |
| [Duplicate an existing campaign](actions/duplicate-an-existing-campaign.md) | POST |  |
| [Edit campaign variables](actions/edit-campaign-variables.md) | PUT |  |
| [Get an email by ID for a specific campaign](actions/get-an-email-by-id-for-a-specific-campaign.md) | GET |  |
| [Get campaign variables](actions/get-campaign-variables.md) | GET |  |
| [Get emails for a specific recipient in a campaign](actions/get-emails-for-a-specific-recipient-in-a-campaign.md) | GET |  |
| [Get landing page details for a campaign](actions/get-landing-page-details-for-a-campaign.md) | GET |  |
| [Import contacts from groups to a campaign](actions/import-contacts-from-groups-to-a-campaign.md) | POST |  |
| [Import contacts to a campaign](actions/import-contacts-to-a-campaign.md) | POST |  |
| [Join a campaign as a guest](actions/join-a-campaign-as-a-guest.md) | POST |  |
| [Preview contacts in segment for campaign](actions/preview-contacts-in-segment-for-campaign.md) | GET |  |
| [Reorder emails in a campaign](actions/reorder-emails-in-a-campaign.md) | PUT |  |
| [Restore draft email to drafts](actions/restore-draft-email-to-drafts.md) | PUT |  |
| [Restore draft email to editing](actions/restore-draft-email-to-editing.md) | GET |  |
| [Retrieve a campaign by ID](actions/retrieve-a-campaign-by-id.md) | GET |  |
| [Retrieve active emails of a campaign](actions/retrieve-active-emails-of-a-campaign.md) | GET |  |
| [Retrieve campaigns](actions/retrieve-campaigns.md) | GET |  |
| [Retrieve data of a campaign](actions/retrieve-data-of-a-campaign.md) | GET |  |
| [Retrieve deleted emails of a campaign](actions/retrieve-deleted-emails-of-a-campaign.md) | GET |  |
| [Retrieve draft emails of a campaign](actions/retrieve-draft-emails-of-a-campaign.md) | GET |  |
| [Retrieve users associated with a campaign](actions/retrieve-users-associated-with-a-campaign.md) | GET |  |
| [Save email draft for a campaign](actions/save-email-draft-for-a-campaign.md) | PUT |  |
| [Send a test mail for the campaign](actions/send-a-test-mail-for-the-campaign.md) | POST |  |
| [Send email to trash](actions/send-email-to-trash.md) | DELETE |  |
| [Set campaign to target a dynamic segment](actions/set-campaign-to-target-a-dynamic-segment.md) | PUT |  |
| [Update campaign interval](actions/update-campaign-interval.md) | PUT |  |
| [Update campaign status](actions/update-campaign-status.md) | PUT |  |
| [Update email configuration for a campaign](actions/update-email-configuration-for-a-campaign.md) | PUT |  |
| [Update email content for a campaign](actions/update-email-content-for-a-campaign.md) | PUT |  |
| [Update landing page details for a campaign](actions/update-landing-page-details-for-a-campaign.md) | PUT |  |

### Chat

| Action | Method | Description |
| --- | --- | --- |
| [Get AI assistant capabilities](actions/get-ai-assistant-capabilities.md) | GET |  |
| [Get suggested prompts for the chat interface](actions/get-suggested-prompts-for-the-chat-interface.md) | GET |  |
| [Send a chat message to the AI assistant](actions/send-a-chat-message-to-the-ai-assistant.md) | POST |  |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Add a contact](actions/add-a-contact.md) | POST |  |
| [Add contacts in bulk to a group](actions/add-contacts-in-bulk-to-a-group.md) | POST |  |
| [Create a new contacts group](actions/create-a-new-contacts-group.md) | POST |  |
| [Delete a contact from a specific group](actions/delete-a-contact-from-a-specific-group.md) | DELETE |  |
| [Delete a contact group](actions/delete-a-contact-group.md) | DELETE |  |
| [Edit a contact](actions/edit-a-contact.md) | PUT |  |
| [Get all contact groups](actions/get-all-contact-groups.md) | GET |  |
| [Get all distinct metadata attribute keys for user's contacts](actions/get-all-distinct-metadata-attribute-keys-for-user-s-contacts.md) | GET |  |
| [Get contact count by attribute filters](actions/get-contact-count-by-attribute-filters.md) | GET |  |
| [Get contacts in a specific group or all contacts](actions/get-contacts-in-a-specific-group-or-all-contacts.md) | GET |  |
| [Manually trigger segment re-evaluation](actions/manually-trigger-segment-re-evaluation.md) | POST |  |
| [Modify contacts by adding them to specified groups and optionally to a campaign.](actions/modify-contacts-by-adding-them-to-specified-groups-and-optionally-to-a-campaign.md) | PUT |  |
| [Remove contacts from a group or delete them entirely (asynchronous).](actions/remove-contacts-from-a-group-or-delete-them-entirely-asynchronous.md) | DELETE |  |
| [Update contact group description](actions/update-contact-group-description.md) | PUT |  |
| [Update metadata attributes for multiple contacts](actions/update-metadata-attributes-for-multiple-contacts.md) | PUT |  |

### Fraudmanagement

| Action | Method | Description |
| --- | --- | --- |
| [Get account health status](actions/get-account-health-status.md) | GET |  |
| [Submit an appeal for account blocking](actions/submit-an-appeal-for-account-blocking.md) | POST |  |

### Identify

| Action | Method | Description |
| --- | --- | --- |
| [Identify a contact and sync attributes from your app](actions/identify-a-contact-and-sync-attributes-from-your-app.md) | POST |  |
| [Platform-internal identify — sync dashboard user attributes](actions/platform-internal-identify-sync-dashboard-user-attributes.md) | POST |  |

### Instantemail

| Action | Method | Description |
| --- | --- | --- |
| [Clone an instant email](actions/clone-an-instant-email.md) | POST |  |
| [Create an instant email](actions/create-an-instant-email.md) | POST |  |
| [Delete instant email by ID](actions/delete-instant-email-by-id.md) | DELETE |  |
| [Edit instant email](actions/edit-instant-email.md) | PUT |  |
| [Get instant email by ID](actions/get-instant-email-by-id.md) | GET |  |
| [Import contact groups to an instant email](actions/import-contact-groups-to-an-instant-email.md) | POST |  |
| [Import CSV contacts to an instant email](actions/import-csv-contacts-to-an-instant-email.md) | POST |  |
| [Retrieve instant emails](actions/retrieve-instant-emails.md) | GET |  |
| [Save email as draft](actions/save-email-as-draft.md) | PUT |  |
| [Send a test mail for an instant email](actions/send-a-test-mail-for-an-instant-email.md) | POST |  |

### Landingpage

| Action | Method | Description |
| --- | --- | --- |
| [Delete a landing page by ID](actions/delete-a-landing-page-by-id.md) | DELETE |  |
| [Get landing page by ID](actions/get-landing-page-by-id.md) | GET |  |
| [Get landing pages](actions/get-landing-pages.md) | GET |  |

### Mcp

| Action | Method | Description |
| --- | --- | --- |
| [Execute an MCP tool](actions/execute-an-mcp-tool.md) | POST |  |
| [Get details about a specific tool](actions/get-details-about-a-specific-tool.md) | GET |  |
| [Get MCP server information and capabilities](actions/get-mcp-server-information-and-capabilities.md) | GET |  |
| [List all available MCP tools](actions/list-all-available-mcp-tools.md) | GET |  |

### Mumara

| Action | Method | Description |
| --- | --- | --- |
| [Add a new sending node to a domain group](actions/add-a-new-sending-node-to-a-domain-group.md) | POST |  |
| [Add a new user to Mumara](actions/add-a-new-user-to-mumara.md) | POST |  |
| [Delete a sending domain from Mumara](actions/delete-a-sending-domain-from-mumara.md) | DELETE |  |
| [Delete a user from Mumara](actions/delete-a-user-from-mumara.md) | DELETE |  |
| [Get details of a specific sending node](actions/get-details-of-a-specific-sending-node.md) | GET |  |
| [Get sending domains from Mumara](actions/get-sending-domains-from-mumara.md) | GET |  |
| [Retrieve sending nodes from Mumara](actions/retrieve-sending-nodes-from-mumara.md) | GET |  |
| [Update a user in Mumara](actions/update-a-user-in-mumara.md) | PUT |  |
| [Update sending node status](actions/update-sending-node-status.md) | PUT |  |

### Mumaradomain

| Action | Method | Description |
| --- | --- | --- |
| [Verify domain DNS records](actions/verify-domain-dns-records.md) | GET |  |

### Mumaraemail

| Action | Method | Description |
| --- | --- | --- |
| [Send email via Mumara](actions/send-email-via-mumara.md) | POST |  |

### Mumarawebhook

| Action | Method | Description |
| --- | --- | --- |
| [Receive webhook from Mumara](actions/receive-webhook-from-mumara.md) | POST |  |

### Oauth

| Action | Method | Description |
| --- | --- | --- |
| [Google OAuth signup or login](actions/google-oauth-signup-or-login.md) | POST |  |

### Onboarding

| Action | Method | Description |
| --- | --- | --- |
| [Send onboarding test mail using dedicated test domains](actions/send-onboarding-test-mail-using-dedicated-test-domains.md) | POST |  |

### Optinpage

| Action | Method | Description |
| --- | --- | --- |
| [Add contact to opt-in page's groups](actions/add-contact-to-opt-in-page-s-groups.md) | POST |  |
| [Atomically create a contact group and attach it to an opt-in page](actions/atomically-create-a-contact-group-and-attach-it-to-an-opt-in-page.md) | POST |  |
| [Atomically create a draft campaign + draft email for an opt-in page](actions/atomically-create-a-draft-campaign-draft-email-for-an-opt-in-page.md) | POST |  |
| [Create a new opt-in page](actions/create-a-new-opt-in-page.md) | POST |  |
| [Delete an opt-in page by ID](actions/delete-an-opt-in-page-by-id.md) | DELETE |  |
| [Get a published opt-in page by ID (public, no auth required)](actions/get-a-published-opt-in-page-by-id-public-no-auth-required.md) | GET |  |
| [Get an opt-in page by ID](actions/get-an-opt-in-page-by-id.md) | GET |  |
| [Get contact counts for an opt-in page's linked groups](actions/get-contact-counts-for-an-opt-in-page-s-linked-groups.md) | GET |  |
| [Get opt-in pages](actions/get-opt-in-pages.md) | GET |  |
| [Get page, setup, checklist, and stats in a single call](actions/get-page-setup-checklist-and-stats-in-a-single-call.md) | GET |  |
| [Get pre-publish checklist for an opt-in page](actions/get-pre-publish-checklist-for-an-opt-in-page.md) | GET |  |
| [Get UTM attribution breakdown for an opt-in page's signups](actions/get-utm-attribution-breakdown-for-an-opt-in-page-s-signups.md) | GET |  |
| [Partially update an opt-in page (e.g. rename)](actions/partially-update-an-opt-in-page-eg-rename.md) | PUT |  |
| [Publish an opt-in page](actions/publish-an-opt-in-page.md) | PUT |  |
| [Unpublish an opt-in page](actions/unpublish-an-opt-in-page.md) | PUT |  |
| [Upload image for an opt-in page](actions/upload-image-for-an-opt-in-page.md) | POST |  |
| [Verify the setup health of an opt-in page](actions/verify-the-setup-health-of-an-opt-in-page.md) | GET |  |

### Payment

| Action | Method | Description |
| --- | --- | --- |
| [Add a new card for the user](actions/add-a-new-card-for-the-user.md) | POST |  |
| [Authorize a transaction](actions/authorize-a-transaction.md) | POST |  |
| [Cancel a subscription](actions/cancel-a-subscription.md) | GET |  |
| [Cancel an active subscription for a user](actions/cancel-an-active-subscription-for-a-user.md) | PUT |  |
| [Create a new subscription for a user](actions/create-a-new-subscription-for-a-user.md) | POST |  |
| [Create a pay-as-you-go transaction](actions/create-a-pay-as-you-go-transaction.md) | POST |  |
| [Create a payment intent](actions/create-a-payment-intent.md) | POST |  |
| [Create a subscription](actions/create-a-subscription.md) | POST |  |
| [Create a top-up transaction](actions/create-a-top-up-transaction.md) | POST |  |
| [Delete a card](actions/delete-a-card.md) | DELETE |  |
| [Delete a user's card](actions/delete-a-user-s-card.md) | DELETE |  |
| [Get top-up rate](actions/get-top-up-rate.md) | GET |  |
| [Get updated pay-as-you-go rate](actions/get-updated-pay-as-you-go-rate.md) | GET |  |
| [Get user's saved cards from Paystack](actions/get-user-s-saved-cards-from-paystack.md) | GET |  |
| [Get user transactions](actions/get-user-transactions.md) | GET |  |
| [Reactivate a canceled subscription for a user](actions/reactivate-a-canceled-subscription-for-a-user.md) | PUT |  |
| [Retrieve the user's saved cards](actions/retrieve-the-user-s-saved-cards.md) | GET |  |
| [Set a card as default](actions/set-a-card-as-default.md) | PUT |  |
| [Set a user's card as the default card](actions/set-a-user-s-card-as-the-default-card.md) | PUT |  |
| [Top up subscription wallet](actions/top-up-subscription-wallet.md) | POST |  |
| [Update a user's subscription plan](actions/update-a-user-s-subscription-plan.md) | PUT |  |
| [Update subscription plan](actions/update-subscription-plan.md) | PUT |  |
| [Validate a payment intent](actions/validate-a-payment-intent.md) | POST |  |
| [Verify a Paystack transaction](actions/verify-a-paystack-transaction.md) | GET |  |

### Plan

| Action | Method | Description |
| --- | --- | --- |
| [Get all available plans](actions/get-all-available-plans.md) | GET |  |

### Promo

| Action | Method | Description |
| --- | --- | --- |
| [Get all active promos](actions/get-all-active-promos.md) | GET |  |
| [Get all available subscription plans with IDs](actions/get-all-available-subscription-plans-with-ids.md) | GET |  |
| [Get promo pricing for a plan (public - all users see promo prices)](actions/get-promo-pricing-for-a-plan-public-all-users-see-promo-prices.md) | GET |  |
| [Record promo usage when user subscribes](actions/record-promo-usage-when-user-subscribes.md) | POST |  |

### Segment

| Action | Method | Description |
| --- | --- | --- |
| [Get segment statistics](actions/get-segment-statistics.md) | GET |  |
| [Preview segment membership without saving](actions/preview-segment-membership-without-saving.md) | GET |  |

### Template

| Action | Method | Description |
| --- | --- | --- |
| [Clone a public template or user-owned template](actions/clone-a-public-template-or-user-owned-template.md) | POST |  |
| [Get public templates with filtering and sorting](actions/get-public-templates-with-filtering-and-sorting.md) | GET |  |
| [Manually regenerate AI review (costs 5 AI credits)](actions/manually-regenerate-ai-review-costs5-ai-credits.md) | POST |  |
| [Rename a user-owned template](actions/rename-a-user-owned-template.md) | PUT |  |
| [Retrieve User Templates](actions/retrieve-user-templates.md) | GET |  |
| [Toggle template public/private (triggers AI review on first publish)](actions/toggle-template-public-private-triggers-ai-review-on-first-publish.md) | PUT |  |

### Transactionalemail

| Action | Method | Description |
| --- | --- | --- |
| [Send a transactional email using a template](actions/send-a-transactional-email-using-a-template.md) | POST |  |
| [Send a transactional email with raw data](actions/send-a-transactional-email-with-raw-data.md) | POST |  |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Change user password](actions/change-user-password.md) | PUT |  |
| [Deactivate the account of the logged-in user](actions/deactivate-the-account-of-the-logged-in-user.md) | PUT |  |
| [Get API credentials](actions/get-api-credentials.md) | GET |  |
| [Get user details](actions/get-user-details.md) | GET |  |
| [Login to the application](actions/login-to-the-application.md) | POST |  |
| [Reactivate a deactivated account](actions/reactivate-a-deactivated-account.md) | POST |  |
| [Register a new user](actions/register-a-new-user.md) | POST |  |
| [Resend verification email](actions/resend-verification-email.md) | POST |  |
| [Reset password using the reset password hash](actions/reset-password-using-the-reset-password-hash.md) | POST |  |
| [Send reset password email](actions/send-reset-password-email.md) | POST |  |
| [Update account settings for the logged-in user](actions/update-account-settings-for-the-logged-in-user.md) | PUT |  |
| [Update email settings for the logged-in user](actions/update-email-settings-for-the-logged-in-user.md) | PUT |  |
| [Update the low credit limit for email credits](actions/update-the-low-credit-limit-for-email-credits.md) | PUT |  |
| [Upload profile photo for the user](actions/upload-profile-photo-for-the-user.md) | POST |  |

