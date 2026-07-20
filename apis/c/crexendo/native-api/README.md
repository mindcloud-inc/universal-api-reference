# Crexendo: Native API Reference

A consolidated summary of Crexendo's API configuration and 30 documented operations, with links to official documentation.

- **Official docs:** https://docs.ns-api.com/reference
- **OpenAPI specification:** https://dash.readme.com/api/v1/api-registry/ma4p2vman3txz9
- **API base URL:** `https://ns-api.com/ns-api/v2`

## Authentication

### API Key

Use a NetSapiens / Crexendo NS API machine-to-machine API key as a bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.ns-api.com/docs/api-keys)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `limit` in the query string to set the page size (default 100; accepted range 1–1000). Use `start` in the query string as the record offset; numbering starts at 0.

## Endpoints (30 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Check Domain Exists](actions/check-domain-exists.md) | `GET /domains/:domain/count` | [docs](https://docs.ns-api.com/reference/countdomain) |
| [Count Domain Active Calls](actions/count-domain-active-calls.md) | `GET /domains/:domain/calls/count` | [docs](https://docs.ns-api.com/reference/get_domains-domain-calls-count) |
| [Count Domains](actions/count-domains.md) | `GET /domains/count` | [docs](https://docs.ns-api.com/reference/countdomains) |
| [Count User Contacts](actions/count-user-contacts.md) | `GET /domains/:domain/users/:user/contacts/count` | [docs](https://docs.ns-api.com/reference/get_domains-domain-users-user-contacts-count) |
| [Count Users](actions/count-users.md) | `GET /domains/:domain/users/count` | [docs](https://docs.ns-api.com/reference/countusers) |
| [Get API Key Info](actions/get-api-key-info.md) | `GET /apikeys/~` | [docs](https://docs.ns-api.com/reference/readmyapikey) |
| [Get Domain](actions/get-domain.md) | `GET /domains/:domain` | [docs](https://docs.ns-api.com/reference/getdomain) |
| [Get Domain Billing Summary](actions/get-domain-billing-summary.md) | `GET /domains/:domain/billing` | [docs](https://docs.ns-api.com/reference/domainbilling) |
| [Get My Domain Info](actions/get-my-domain-info.md) | `GET /domains/~` | [docs](https://docs.ns-api.com/reference/getmydomain) |
| [Get My User](actions/get-my-user.md) | `GET /domains/~/users/~` | [docs](https://docs.ns-api.com/reference/getmyuser) |
| [Get User](actions/get-user.md) | `GET /domains/:domain/users/:user` | [docs](https://docs.ns-api.com/reference/getuser) |
| [List Call Queues](actions/list-call-queues.md) | `GET /domains/:domain/callqueues` | [docs](https://docs.ns-api.com/reference/readcallqueues) |
| [List Domain Active Calls](actions/list-domain-active-calls.md) | `GET /domains/:domain/calls` | [docs](https://docs.ns-api.com/reference/get_domains-domain-calls) |
| [List Domain Addresses](actions/list-domain-addresses.md) | `GET /domains/:domain/addresses` | [docs](https://docs.ns-api.com/reference/getaddressesfordomain) |
| [List Domain Agents](actions/list-domain-agents.md) | `GET /domains/:domain/agents` | [docs](https://docs.ns-api.com/reference/readagentsdomain) |
| [List Domain Contacts](actions/list-domain-contacts.md) | `GET /domains/:domain/contacts` | [docs](https://docs.ns-api.com/reference/getdomaincontacts) |
| [List Domain Phone Numbers](actions/list-domain-phone-numbers.md) | `GET /domains/:domain/phonenumbers` | [docs](https://docs.ns-api.com/reference/getdomainphonenumbers) |
| [List Domain SMS Numbers](actions/list-domain-sms-numbers.md) | `GET /domains/:domain/smsnumbers` | [docs](https://docs.ns-api.com/reference/getsmsnumbersfordomain) |
| [List Domains](actions/list-domains.md) | `GET /domains` | [docs](https://docs.ns-api.com/reference/getdomains) |
| [List My Answer Rules](actions/list-my-answer-rules.md) | `GET /domains/~/users/~/answerrules` | [docs](https://docs.ns-api.com/reference/get_domains-users-answerrules) |
| [List My Contacts](actions/list-my-contacts.md) | `GET /domains/~/users/~/contacts` | [docs](https://docs.ns-api.com/reference/get_domains-users-contacts) |
| [List Phone Numbers](actions/list-phone-numbers.md) | `GET /phonenumbers` | [docs](https://docs.ns-api.com/reference/getphonenumbers) |
| [List Sites](actions/list-sites.md) | `GET /domains/:domain/sites` | [docs](https://docs.ns-api.com/reference/get_domains-domain-sites) |
| [List User Active Calls](actions/list-user-active-calls.md) | `GET /domains/:domain/users/:user/calls` | [docs](https://docs.ns-api.com/reference/get_domains-domain-users-user-calls) |
| [List User Addresses](actions/list-user-addresses.md) | `GET /domains/:domain/users/:user/addresses` | [docs](https://docs.ns-api.com/reference/getaddressesforuser) |
| [List User Contacts](actions/list-user-contacts.md) | `GET /domains/:domain/users/:user/contacts` | [docs](https://docs.ns-api.com/reference/get_domains-domain-users-user-contacts) |
| [List User Devices](actions/list-user-devices.md) | `GET /domains/:domain/users/:user/devices` | [docs](https://docs.ns-api.com/reference/getdevices) |
| [List User Meetings](actions/list-user-meetings.md) | `GET /domains/:domain/users/:user/meetings` | [docs](https://docs.ns-api.com/reference/get_domains-domain-users-user-meetings) |
| [List User SMS Numbers](actions/list-user-sms-numbers.md) | `GET /domains/:domain/users/:user/smsnumbers` | [docs](https://docs.ns-api.com/reference/getsmsnumbersforuser) |
| [List Users](actions/list-users.md) | `GET /domains/:domain/users` | [docs](https://docs.ns-api.com/reference/getusers) |
