# Reply: Native API Reference

A consolidated summary of Reply's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://apidocs.reply.io/
- **API base URL:** `https://api.reply.io`

## Authentication

### API Key

Use your Reply personal API key from Settings > API Key.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
x-api-key: <apiKey>
```

[Official authentication documentation](https://apidocs.reply.io/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

The total page count is read from `pagesCount`. The current page number is read from `page`.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Campaign](actions/create-campaign.md) | `POST /v2/campaigns` | [docs](https://apidocs.reply.io/) |
| [Create List](actions/create-list.md) | `POST /v1/people/lists` | [docs](https://apidocs.reply.io/) |
| [Create New Contact](actions/create-new-contact.md) | `POST /v1/people` | [docs](https://apidocs.reply.io/) |
| [Delete Contact By Id](actions/delete-contact-by-id.md) | `DELETE /v1/people` | [docs](https://apidocs.reply.io/) |
| [Get All Contacts](actions/get-all-contacts.md) | `GET /v1/people` | [docs](https://apidocs.reply.io/) |
| [Get All Lists](actions/get-all-lists.md) | `GET /v1/people/lists` | [docs](https://apidocs.reply.io/) |
| [Get Campaign By Id](actions/get-campaign-by-id.md) | `GET /v1/campaigns` | [docs](https://apidocs.reply.io/) |
| [Get Contact By Email](actions/get-contact-by-email.md) | `GET /v1/people` | [docs](https://apidocs.reply.io/) |
| [Get Contact By Id](actions/get-contact-by-id.md) | `GET /v1/people` | [docs](https://apidocs.reply.io/) |
| [Get Contacts In List](actions/get-contacts-in-list.md) | `GET /v1/people/list/:listId` | [docs](https://apidocs.reply.io/) |
| [Get Custom Fields](actions/get-custom-fields.md) | `GET /v1/custom-fields/all` | [docs](https://apidocs.reply.io/) |
| [Get Email Accounts](actions/get-email-accounts.md) | `GET /v1/emailAccounts` | [docs](https://apidocs.reply.io/) |
| [Get List of Campaigns](actions/get-list-of-campaigns.md) | `GET /v1/campaigns` | [docs](https://apidocs.reply.io/) |
| [Get Schedules](actions/get-schedules.md) | `GET /v2/schedules` | [docs](https://apidocs.reply.io/) |
| [Get Templates](actions/get-templates.md) | `GET /v1/templates` | [docs](https://apidocs.reply.io/) |
| [Lookup Prospect Id](actions/lookup-prospect-id.md) | `POST /v1/people/lookup` | [docs](https://apidocs.reply.io/) |
| [Move Contact To List](actions/move-contact-to-list.md) | `POST /v1/Actions/moveContactsToLists` | [docs](https://apidocs.reply.io/) |
| [Pause Campaign](actions/pause-campaign.md) | `POST /v2/campaigns/:campaignId/pause` | [docs](https://apidocs.reply.io/) |
| [Push Contact To Sequence](actions/push-contact-to-sequence.md) | `POST /v1/actions/pushtocampaign` | [docs](https://apidocs.reply.io/) |
| [Remove Contact From Sequence](actions/remove-contact-from-sequence.md) | `POST /v1/actions/removepersonfromcampaignbyid` | [docs](https://apidocs.reply.io/) |
| [Send Direct Email To Prospect](actions/send-direct-email-to-prospect.md) | `POST /v2/prospects/:prospectid/emails` | [docs](https://apidocs.reply.io/) |
| [Start Campaign](actions/start-campaign.md) | `POST /v2/campaigns/:campaignId/start` | [docs](https://apidocs.reply.io/) |
| [Update Campaign Settings](actions/update-campaign-settings.md) | `PATCH /v2/campaigns/:campaignId` | [docs](https://apidocs.reply.io/) |
| [Update Contact By Email](actions/update-contact-by-email.md) | `POST /v1/people` | [docs](https://apidocs.reply.io/) |
