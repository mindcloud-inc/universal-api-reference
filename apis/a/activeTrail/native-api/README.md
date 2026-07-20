# ActiveTrail: Native API Reference

A consolidated summary of ActiveTrail's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://webapi.mymarketing.co.il/api/docs/Guides
- **API base URL:** `https://webapi.mymarketing.co.il/api`

## Authentication

### API Token

Use an ActiveTrail access token generated from the API Apps settings.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://www.activetrail.com/integrations/learning/guides/a-guide-to-accessing-activetrails-restful-api/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Pagination

Use `Limit` in the query string to set the page size (default 20; accepted range 1–100). Use `Page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Contact to Group](actions/add-contact-to-group.md) | `POST /groups/:id/members` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-groups-id-members) |
| [Create Contact](actions/create-contact.md) | `POST /contacts` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-contacts) |
| [Create Group](actions/create-group.md) | `POST /groups` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-groups) |
| [Create Mailing List](actions/create-mailing-list.md) | `POST /mailinglist` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-mailinglist) |
| [Delete Contact](actions/delete-contact.md) | `DELETE /contacts/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/DELETE-api-contacts-id) |
| [Delete Group](actions/delete-group.md) | `DELETE /groups/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/DELETE-api-groups-id) |
| [Delete Mailing List](actions/delete-mailing-list.md) | `DELETE /mailinglist/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/DELETE-api-mailinglist-id) |
| [Get Account Balance](actions/get-account-balance.md) | `GET /account/balance` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-account-balance) |
| [Get Campaign](actions/get-campaign.md) | `GET /campaigns/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-campaigns-id) |
| [Get Contact](actions/get-contact.md) | `GET /contacts/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-contacts-id) |
| [Get Group](actions/get-group.md) | `GET /groups/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-groups-Id) |
| [Get Mailing List](actions/get-mailing-list.md) | `GET /mailinglist/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-mailinglist-Id) |
| [Import Contacts](actions/import-contacts.md) | `POST /contacts/Import` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-contacts-Import) |
| [List Campaigns](actions/list-campaigns.md) | `GET /campaigns` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-campaigns_MailingListId_ContentCategoryId_SearchTerm_SendType_FromDate_ToDate_Page_Limit) |
| [List Contacts](actions/list-contacts.md) | `GET /contacts` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-contacts_CustomerStates_SearchTerm_FromDate_ToDate_Page_Limit) |
| [List Group Members](actions/list-group-members.md) | `GET /groups/:id/members` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-groups-id-members_CustomerStates_SearchTerm_FromDate_ToDate_Page_Limit) |
| [List Groups](actions/list-groups.md) | `GET /groups` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-groups_SearchTerm_Page_Limit) |
| [List Mailing Lists](actions/list-mailing-lists.md) | `GET /mailinglist` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/GET-api-mailinglist) |
| [Remove Member from Group](actions/remove-member-from-group.md) | `DELETE /groups/:id/members/:memberId` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/DELETE-api-groups-id-members-memberId) |
| [Send Email Operational Message to Contacts](actions/send-email-operational-message-to-contacts.md) | `POST /OperationalMessage/Contacts` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/POST-api-OperationalMessage-Contacts) |
| [Update Campaign](actions/update-campaign.md) | `PUT /campaigns/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/PUT-api-campaigns-id) |
| [Update Contact](actions/update-contact.md) | `PUT /contacts/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/PUT-api-contacts-id) |
| [Update Group](actions/update-group.md) | `PUT /groups/:id` | [docs](https://webapi.mymarketing.co.il/api/docs/and/Api/PUT-api-groups-id) |
