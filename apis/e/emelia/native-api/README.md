# Emelia: Native API Reference

A consolidated summary of Emelia's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://docs-old.emelia.io/
- **API base URL:** `https://graphql.emelia.io`

## Authentication

### API Key

Authenticate with your Emelia API key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs-old.emelia.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact To Campaign](actions/add-contact-to-campaign.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-add_contact_to_a_campaign-post) |
| [Add Contact To List](actions/add-contact-to-list.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-add_contact_to_a_list-post) |
| [Add Webhook To Scrap](actions/add-webhook-to-scrap.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-add_webhook_to_a_scrap-post) |
| [Create Campaign](actions/create-campaign.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-create_a_campaign-post) |
| [Create Credential](actions/create-credential.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-create_credential-post) |
| [Download Scrap](actions/download-scrap.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-download_a_scrap-post) |
| [Get Campaign](actions/get-campaign.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-get_a_campaign-post) |
| [Get User Data](actions/get-user-data.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-get_user_data-post) |
| [Launch Scrap](actions/launch-scrap.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-launch_a_scrap-post) |
| [List Campaigns](actions/list-campaigns.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-get_campaigns-post) |
| [List Contact Lists](actions/list-contact-lists.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-get_contacts_lists-post) |
| [List Credentials](actions/list-credentials.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-get_credentials-post) |
| [List Scraps](actions/list-scraps.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-get_scraps-post) |
| [Pause Campaign](actions/pause-campaign.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-pause_a_campaign-post) |
| [Pause Scrap](actions/pause-scrap.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-pause_a_scrap-post) |
| [Remove Contact From Campaign](actions/remove-contact-from-campaign.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-remove_contact_from_a_campaign-post) |
| [Remove Webhook From Scrap](actions/remove-webhook-from-scrap.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-remove_webhook_to_a_scrap-post) |
| [Resume Scrap](actions/resume-scrap.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-resume_a_scrap-post) |
| [Start Campaign](actions/start-campaign.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-start_a_campaign-post) |
| [Update Credential](actions/update-credential.md) | `POST /graphql` | [docs](https://docs-old.emelia.io/#operation-update_credential-post) |
