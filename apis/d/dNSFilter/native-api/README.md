# DNSFilter: Native API Reference

A consolidated summary of DNSFilter's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://api.dnsfilter.com/docs
- **OpenAPI specification:** https://api.dnsfilter.com/docs/api.json
- **API base URL:** `https://api.dnsfilter.com`

## Authentication

### API Key

Use a DNSFilter API key in the Authorization header.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: <apiKey>
```

[Official authentication documentation](https://api.dnsfilter.com/docs)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `page[size]` in the query string to set the page size (default 100; minimum 1). Use `page[number]` in the query string to choose the page; numbering starts at 1.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Bulk Lookup Domains](actions/bulk-lookup-domains.md) | `GET /v1/domains/bulk_lookup` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1domains~1bulk_lookup/get) |
| [Get Application](actions/get-application.md) | `GET /v1/applications/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1applications~1{id}/get) |
| [Get Application Category](actions/get-application-category.md) | `GET /v1/application_categories/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1application_categories~1{id}/get) |
| [Get Block Page](actions/get-block-page.md) | `GET /v1/block_pages/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1block_pages~1{id}/get) |
| [Get Category](actions/get-category.md) | `GET /v1/categories/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1categories~1{id}/get) |
| [Get Current User](actions/get-current-user.md) | `GET /v1/current_user` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1current_user/get) |
| [Get Domain Note](actions/get-domain-note.md) | `GET /v1/notes/:resource/:id/:domain` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1notes~1{resource}~1{id}~1{domain}/get) |
| [Get IP Address](actions/get-ip-address.md) | `GET /v1/ip_addresses/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1ip_addresses~1{id}/get) |
| [Get MAC Address](actions/get-mac-address.md) | `GET /v1/mac_addresses/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1mac_addresses~1{id}/get) |
| [Get Network](actions/get-network.md) | `GET /v1/networks/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1networks~1{id}/get) |
| [Get Network Counts](actions/get-network-counts.md) | `GET /v1/networks/counts` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1networks~1counts/get) |
| [Get Network Geo](actions/get-network-geo.md) | `GET /v1/networks/geo` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1networks~1geo/get) |
| [Get Network Subnet](actions/get-network-subnet.md) | `GET /v1/networks/:id/subnets/:subnet_id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1networks~1{id}~1subnets~1{subnet_id}/get) |
| [Get Organization](actions/get-organization.md) | `GET /v1/organizations/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1organizations~1{id}/get) |
| [Get Organization Settings](actions/get-organization-settings.md) | `GET /v1/organizations/settings` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1organizations~1settings/get) |
| [Get Organization User](actions/get-organization-user.md) | `GET /v1/organizations/:organization_id/users/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1organizations~1{organization_id}~1users~1{id}/get) |
| [Get Policy](actions/get-policy.md) | `GET /v1/policies/:id` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1policies~1{id}/get) |
| [Get Policy Application](actions/get-policy-application.md) | `GET /v1/policies/application` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1policies~1application/get) |
| [Get Policy Permissive Mode](actions/get-policy-permissive-mode.md) | `GET /v1/policies/:id/permissive_mode` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1policies~1{id}~1permissive_mode/get) |
| [List All Applications](actions/list-all-applications.md) | `GET /v1/applications/all` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1applications~1all/get) |
| [List All Categories](actions/list-all-categories.md) | `GET /v1/categories/all` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1categories~1all/get) |
| [List All IP Addresses](actions/list-all-ip-addresses.md) | `GET /v1/ip_addresses/all` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1ip_addresses~1all/get) |
| [List All MAC Addresses](actions/list-all-mac-addresses.md) | `GET /v1/mac_addresses/all` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1mac_addresses~1all/get) |
| [List All Networks](actions/list-all-networks.md) | `GET /v1/networks/all` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1networks~1all/get) |
| [List All Organizations](actions/list-all-organizations.md) | `GET /v1/organizations/all` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1organizations~1all/get) |
| [List All Policies](actions/list-all-policies.md) | `GET /v1/policies/all` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1policies~1all/get) |
| [List Application Categories](actions/list-application-categories.md) | `GET /v1/application_categories` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1application_categories/get) |
| [List Applications](actions/list-applications.md) | `GET /v1/applications` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1applications/get) |
| [List Block Pages](actions/list-block-pages.md) | `GET /v1/block_pages` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1block_pages/get) |
| [List Categories](actions/list-categories.md) | `GET /v1/categories` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1categories/get) |
| [List IP Addresses](actions/list-ip-addresses.md) | `GET /v1/ip_addresses` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1ip_addresses/get) |
| [List MAC Addresses](actions/list-mac-addresses.md) | `GET /v1/mac_addresses` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1mac_addresses/get) |
| [List Network Subnets](actions/list-network-subnets.md) | `GET /v1/networks/:id/subnets` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1networks~1{id}~1subnets/get) |
| [List Networks](actions/list-networks.md) | `GET /v1/networks` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1networks/get) |
| [List Organization Users](actions/list-organization-users.md) | `GET /v1/organizations/:organization_id/users` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1organizations~1{organization_id}~1users/get) |
| [List Organizations](actions/list-organizations.md) | `GET /v1/organizations` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1organizations/get) |
| [List Policies](actions/list-policies.md) | `GET /v1/policies` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1policies/get) |
| [Lookup Domain](actions/lookup-domain.md) | `GET /v1/domains/user_lookup` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1domains~1user_lookup/get) |
| [Lookup Network](actions/lookup-network.md) | `GET /v1/networks/lookup` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1networks~1lookup/get) |
| [Verify IP Address](actions/verify-ip-address.md) | `GET /v1/ip_addresses/verify` | [docs](https://api.dnsfilter.com/docs#/paths/~1v1~1ip_addresses~1verify/get) |
