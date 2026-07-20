# Snapchat Lead Generation: Native API Reference

A consolidated summary of Snapchat Lead Generation's API configuration and 9 documented operations, with links to official documentation.

- **Official docs:** https://developers.snap.com/api/marketing-api/Ads-API/introduction
- **API base URL:** `https://adsapi.snapchat.com/v1`

## Authentication

### OAuth2

Authenticate with a Snapchat Marketing API OAuth app and authorize MindCloud to act on behalf of a Snapchat business user.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://accounts.snapchat.com/login/oauth2/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://accounts.snapchat.com/login/oauth2/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `snapchat-marketing-api`.

The flow supports refresh tokens. Refresh expired access tokens with a POST request to https://accounts.snapchat.com/login/oauth2/access_token.

[Official authentication documentation](https://developers.snap.com/api/marketing-api/Ads-API/authentication)

## Endpoints (9 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lead Generation Ad](actions/create-lead-generation-ad.md) | `POST /adsquads/:adSquadId/ads` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#creating-a-lead-generation-ad-using-a-creative) |
| [Create Lead Generation Creative](actions/create-lead-generation-creative.md) | `POST /adaccounts/:adAccountId/creatives` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#creating-a-lead-generation-creative-using-a-lead-generation-form) |
| [Create Lead Generation Form](actions/create-lead-generation-form.md) | `POST /adaccounts/:adAccountId/lead_generation_forms` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#creating-a-lead-generation-form) |
| [Create Webhook Integration](actions/create-webhook-integration.md) | `POST /lead_gen/integrations/public_webhook` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#create-a-new-webhook-integration) |
| [Delete Webhook Integration](actions/delete-webhook-integration.md) | `DELETE /lead_gen/integrations/:integrationId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#delete-a-webhook-integration) |
| [Get Lead Generation Form](actions/get-lead-generation-form.md) | `GET /lead_generation_forms/:leadGenerationFormId` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#get-lead-generation-form-using-lead-generation-id) |
| [List Lead Generation Forms](actions/list-lead-generation-forms.md) | `GET /adaccounts/:adAccountId/lead_generation_forms` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#get-lead-generation-forms-under-an-ad-account) |
| [List Webhook Integrations](actions/list-webhook-integrations.md) | `GET /lead_gen/forms/:formId/integrations` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#get-all-webhook-integrations-under-a-form) |
| [Send Test Lead Data](actions/send-test-lead-data.md) | `GET /lead_gen/integrations/:integrationId/test` | [docs](https://developers.snap.com/api/marketing-api/Ads-API/lead-generation-ads#send-test-lead-data) |
