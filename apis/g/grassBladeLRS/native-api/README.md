# GrassBlade LRS: Native API Reference

A consolidated summary of GrassBlade LRS's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://github.com/adlnet/xAPI-Spec/tree/xAPI-1.0.3
- **API base URL:** `https://test.gblrs.com/xAPI`

## Authentication

### Basic AuthToken

Connect with the GrassBlade xAPI API user and API password.

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

[Official authentication documentation](https://www.nextsoftwaresolutions.com/kb/connect-grassblade-lrs-with-grassblade-xapi-companion/)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |
| `X-Experience-API-Version` | `1.0.3` |

Responses from this API use JSON.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Activity Profile](actions/create-activity-profile.md) | `POST /activities/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#actprofres) |
| [Create Agent Profile](actions/create-agent-profile.md) | `POST /agents/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentprofres) |
| [Create State Document](actions/create-state-document.md) | `POST /activities/state` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres) |
| [Create Statement](actions/create-statement.md) | `POST /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtrespost) |
| [Create Statement Batch](actions/create-statement-batch.md) | `POST /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtrespost) |
| [Create Statement By ID](actions/create-statement-by-id.md) | `PUT /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresput) |
| [Delete Activity Profile](actions/delete-activity-profile.md) | `DELETE /activities/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#actprofres) |
| [Delete Agent Profile](actions/delete-agent-profile.md) | `DELETE /agents/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentprofres) |
| [Delete All State For Context](actions/delete-all-state-for-context.md) | `DELETE /activities/state` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres) |
| [Delete State Document](actions/delete-state-document.md) | `DELETE /activities/state` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres) |
| [Get About](actions/get-about.md) | `GET /about` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md) |
| [Get Activity By ID](actions/get-activity-by-id.md) | `GET /activities` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#activitiesres) |
| [Get Activity Profile](actions/get-activity-profile.md) | `GET /activities/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#actprofres) |
| [Get Agent Profile](actions/get-agent-profile.md) | `GET /agents/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentprofres) |
| [Get Person By Agent](actions/get-person-by-agent.md) | `GET /agents` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentsres) |
| [Get State Document](actions/get-state-document.md) | `GET /activities/state` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres) |
| [Get Statement By ID](actions/get-statement-by-id.md) | `GET /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget) |
| [Get Voided Statement](actions/get-voided-statement.md) | `GET /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget) |
| [List Activity Profile IDs](actions/list-activity-profile-ids.md) | `GET /activities/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#actprofres) |
| [List Activity Profile IDs Since](actions/list-activity-profile-ids-since.md) | `GET /activities/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#actprofres) |
| [List Agent Profile IDs](actions/list-agent-profile-ids.md) | `GET /agents/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentprofres) |
| [List Agent Profile IDs Since](actions/list-agent-profile-ids-since.md) | `GET /agents/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentprofres) |
| [List State IDs](actions/list-state-ids.md) | `GET /activities/state` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres) |
| [List State IDs Since](actions/list-state-ids-since.md) | `GET /activities/state` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres) |
| [List Statements](actions/list-statements.md) | `GET /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget) |
| [Replace Activity Profile](actions/replace-activity-profile.md) | `PUT /activities/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#actprofres) |
| [Replace Agent Profile](actions/replace-agent-profile.md) | `PUT /agents/profile` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#agentprofres) |
| [Replace State Document](actions/replace-state-document.md) | `PUT /activities/state` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stateres) |
| [Search Statements By Activity](actions/search-statements-by-activity.md) | `GET /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget) |
| [Search Statements By Agent](actions/search-statements-by-agent.md) | `GET /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget) |
| [Search Statements By Registration](actions/search-statements-by-registration.md) | `GET /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget) |
| [Search Statements By Time Window](actions/search-statements-by-time-window.md) | `GET /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget) |
| [Search Statements By Verb](actions/search-statements-by-verb.md) | `GET /statements` | [docs](https://github.com/adlnet/xAPI-Spec/blob/xAPI-1.0.3/xAPI-Communication.md#stmtresget) |
