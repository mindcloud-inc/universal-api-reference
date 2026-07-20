# PBX Yeastar: Native API Reference

A consolidated summary of PBX Yeastar's API configuration and 14 documented operations, with links to official documentation.

- **Official docs:** https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/about-this-guide.html
- **API base URL:** `{baseUrl}/openapi/v1.0`

## Authentication

### OAuth2 Machine-to-Machine

Authenticate to a Yeastar P-Series Cloud PBX using the PBX API Client ID and Client Secret.

### Credentials

- **PBX Base URL:** `baseUrl` · required · Base URL of the Yeastar Central Management tenant, for example https://example.use.ycmcloud.com.

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Exchange the returned authorization code with a POST request to {{credentials.baseUrl}}/openapi/v1.0/get_token.
2. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.


The flow supports refresh tokens. Refresh expired access tokens with a POST request to {{credentials.baseUrl}}/openapi/v1.0/refresh_token. A machine-to-machine flow is configured.

[Official authentication documentation](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/get-access-token.html)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `User-Agent` | `OpenAPI` |

Responses from this API use JSON.

## Pagination

Use `page_size` in the query string to set the page size (default 50; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort_by` in the query string. Set the direction separately with `order_by`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 500 ms before the first retry. Stop after 2 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (14 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Menu Options](actions/get-menu-options.md) | `GET /system/get_menuoptions` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/get-menu-options.html) |
| [Query Company Contact List](actions/query-company-contact-list.md) | `GET /company_contact/list` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/query-company-contacts-list.html) |
| [Query Extension List](actions/query-extension-list.md) | `GET /extension/list` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/query-extension-list.html) |
| [Query PBX Capacity](actions/query-pbx-capacity.md) | `GET /system/capacity` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/query-pbx-capacity.html) |
| [Query PBX Information](actions/query-pbx-information.md) | `GET /system/information` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/query-pbx-information.html) |
| [Query Phonebook](actions/query-phonebook.md) | `GET /phonebook/get` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/query-information-of-a-phonebook.html) |
| [Query Phonebook List](actions/query-phonebook-list.md) | `GET /phonebook/list` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/query-phonebook-list.html) |
| [Query Queue List](actions/query-queue-list.md) | `GET /queue/list` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/query-queue-list.html) |
| [Query Trunk List](actions/query-trunk-list.md) | `GET /trunk/list` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/query-trunk-list.html) |
| [Search Company Contacts](actions/search-company-contacts.md) | `GET /company_contact/search` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/search-specific-company-contacts.html) |
| [Search Extensions](actions/search-extensions.md) | `GET /extension/search` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/search-specific-extensions.html) |
| [Search Phonebooks](actions/search-phonebooks.md) | `GET /phonebook/search` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/search-specific-phonebooks.html) |
| [Search Queues](actions/search-queues.md) | `GET /queue/search` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/search-specific-queues.html) |
| [Search Trunks](actions/search-trunks.md) | `GET /trunk/search` | [docs](https://help.yeastar.com/en/p-series-cloud-edition/developer-guide/search-specfic-trunks.html) |
