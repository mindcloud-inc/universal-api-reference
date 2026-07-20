# Veracity Learning: Native API Reference

A consolidated summary of Veracity Learning's API configuration and 25 documented operations, with links to official documentation.

- **Official docs:** https://oliver.enterprise.lrs.io/docs/manual/basics/
- **API base URL:** `https://sample-lrs-rafehwe.lrs.io/xapi`

## Authentication

### Basic

Connect to Veracity Learning xAPI with an xAPI access key username and password.

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

[Official authentication documentation](https://oliver.enterprise.lrs.io/docs/manual/basics/)

## API conventions

Shared headers:

| Header | Value |
| --- | --- |
| `X-Experience-API-Version` | `1.0.3` |

The next-page cursor is read from `more`.

## Pagination

Use `limit` in the query string to set the page size.

## Endpoints (25 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Statements](actions/create-statements.md) | `POST /statements` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Delete Activity Profile Document](actions/delete-activity-profile-document.md) | `DELETE /activities/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Delete Agent Profile Document](actions/delete-agent-profile-document.md) | `DELETE /agents/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Delete All State Documents](actions/delete-all-state-documents.md) | `DELETE /activities/state` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Delete State Document](actions/delete-state-document.md) | `DELETE /activities/state` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Get Activity](actions/get-activity.md) | `GET /activities` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Get Activity Profile Document](actions/get-activity-profile-document.md) | `GET /activities/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Get Agent](actions/get-agent.md) | `GET /agents` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Get Agent Profile Document](actions/get-agent-profile-document.md) | `GET /agents/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Get LRS About](actions/get-lrs-about.md) | `GET /about` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Get More Statements](actions/get-more-statements.md) | `GET /statements/more` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Get State Document](actions/get-state-document.md) | `GET /activities/state` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Get Statement](actions/get-statement.md) | `GET /statements` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Get Voided Statement](actions/get-voided-statement.md) | `GET /statements` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [List Activity Profile IDs](actions/list-activity-profile-ids.md) | `GET /activities/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [List Agent Profile IDs](actions/list-agent-profile-ids.md) | `GET /agents/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [List State IDs](actions/list-state-ids.md) | `GET /activities/state` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [List Statements](actions/list-statements.md) | `GET /statements` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Merge Activity Profile Document](actions/merge-activity-profile-document.md) | `POST /activities/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Merge Agent Profile Document](actions/merge-agent-profile-document.md) | `POST /agents/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Merge State Document](actions/merge-state-document.md) | `POST /activities/state` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Put Activity Profile Document](actions/put-activity-profile-document.md) | `PUT /activities/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Put Agent Profile Document](actions/put-agent-profile-document.md) | `PUT /agents/profile` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Put State Document](actions/put-state-document.md) | `PUT /activities/state` | [docs](https://xapi.ieee-saopen.org/standard/) |
| [Put Statement](actions/put-statement.md) | `PUT /statements` | [docs](https://xapi.ieee-saopen.org/standard/) |
