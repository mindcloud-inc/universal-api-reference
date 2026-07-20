# Unbounce: Native API Reference

A consolidated summary of Unbounce's API configuration and 18 documented operations, with links to official documentation.

- **Official docs:** https://developer.unbounce.com/api_reference/
- **API base URL:** `https://api.unbounce.com`

## Authentication

### Basic Auth

Authenticate to Unbounce with HTTP Basic Auth using your API key as the username and a blank password.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://developer.unbounce.com/getting_started/#api-keys)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/vnd.unbounce.api.v0.4+json` |

Responses from this API use JSON. Response data is read from `accounts`.

## Endpoints (18 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Lead Deletion Request](actions/create-lead-deletion-request.md) | `POST /pages/:page_id/lead_deletion_request` | [docs](https://developer.unbounce.com/api_reference/#id_pages__page_id__lead_deletion_request) |
| [Create Page Lead](actions/create-page-lead.md) | `POST /pages/:page_id/leads` | [docs](https://developer.unbounce.com/api_reference/#id_pages__page_id__leads) |
| [Delete Page Lead](actions/delete-page-lead.md) | `DELETE /pages/:page_id/leads/:lead_id` | [docs](https://developer.unbounce.com/api_reference/#id_pages__page_id__leads__lead_id_) |
| [Get Lead](actions/get-lead.md) | `GET /leads/:lead_id` | [docs](https://developer.unbounce.com/api_reference/#id_leads__lead_id_) |
| [Get Page Lead](actions/get-page-lead.md) | `GET /pages/:page_id/leads/:lead_id` | [docs](https://developer.unbounce.com/api_reference/#id_pages__page_id__leads__lead_id_) |
| [List Account Pages](actions/list-account-pages.md) | `GET /accounts/:account_id/pages` | [docs](https://developer.unbounce.com/api_reference/#id_accounts__account_id__pages) |
| [List Account Sub Accounts](actions/list-account-sub-accounts.md) | `GET /accounts/:account_id/sub_accounts` | [docs](https://developer.unbounce.com/api_reference/#id_accounts__account_id__sub_accounts) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts` | [docs](https://developer.unbounce.com/api_reference/#id_accounts) |
| [List Page Form Fields](actions/list-page-form-fields.md) | `GET /pages/:page_id/form_fields` | [docs](https://developer.unbounce.com/api_reference/#id_pages__page_id__form_fields) |
| [List Page Group Pages](actions/list-page-group-pages.md) | `GET /page_groups/:page_group_id/pages` | [docs](https://developer.unbounce.com/api_reference/#id_page_groups__page_group_id__pages) |
| [List Page Leads](actions/list-page-leads.md) | `GET /pages/:page_id/leads` | [docs](https://developer.unbounce.com/api_reference/#id_pages__page_id__leads) |
| [List Pages](actions/list-pages.md) | `GET /pages` | [docs](https://developer.unbounce.com/api_reference/#id_pages) |
| [List Sub Account Page Groups](actions/list-sub-account-page-groups.md) | `GET /sub_accounts/:sub_account_id/page_groups` | [docs](https://developer.unbounce.com/api_reference/#id_sub_accounts__sub_account_id__page_groups) |
| [List Sub Account Pages](actions/list-sub-account-pages.md) | `GET /sub_accounts/:sub_account_id/pages` | [docs](https://developer.unbounce.com/api_reference/#id_sub_accounts__sub_account_id__pages) |
| [Retrieve Account](actions/retrieve-account.md) | `GET /accounts/:account_id` | [docs](https://developer.unbounce.com/api_reference/#id_accounts__account_id_) |
| [Retrieve Lead Deletion Request](actions/retrieve-lead-deletion-request.md) | `GET /pages/:page_id/lead_deletion_request/:lead_deletion_request_id` | [docs](https://developer.unbounce.com/api_reference/#id_pages__page_id__lead_deletion_request__lead_deletion_request_id_) |
| [Retrieve Page](actions/retrieve-page.md) | `GET /pages/:page_id` | [docs](https://developer.unbounce.com/api_reference/#id_pages__page_id_) |
| [Retrieve Sub Account](actions/retrieve-sub-account.md) | `GET /sub_accounts/:sub_account_id` | [docs](https://developer.unbounce.com/api_reference/#id_sub_accounts__sub_account_id_) |
