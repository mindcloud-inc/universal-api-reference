# LeadIQ: Native API Reference

A consolidated summary of LeadIQ's API configuration and 6 documented operations, with links to official documentation.

- **Official docs:** https://developer.leadiq.com/
- **API base URL:** `https://api.leadiq.com/`

## Authentication

### Basic

Use your LeadIQ Secret API key as the Basic username. Leave password blank.

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

[Official authentication documentation](https://leadiqhelp.zendesk.com/hc/en-us/articles/29375289152795-LeadIQ-Public-API-Guide)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Endpoints (6 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Flat Advanced Search](actions/flat-advanced-search.md) | `POST graphql` | [docs](https://developer.leadiq.com/#query-flatAdvancedSearch) |
| [Get Account](actions/get-account.md) | `POST graphql` | [docs](https://developer.leadiq.com/#query-account) |
| [Grouped Advanced Search](actions/grouped-advanced-search.md) | `POST graphql` | [docs](https://developer.leadiq.com/#query-groupedAdvancedSearch) |
| [Search Company](actions/search-company.md) | `POST graphql` | [docs](https://developer.leadiq.com/#query-searchCompany) |
| [Search People](actions/search-people.md) | `POST graphql` | [docs](https://developer.leadiq.com/#query-searchPeople) |
| [Submit Person Feedback](actions/submit-person-feedback.md) | `POST graphql` | [docs](https://developer.leadiq.com/#mutation-submitPersonFeedback) |
