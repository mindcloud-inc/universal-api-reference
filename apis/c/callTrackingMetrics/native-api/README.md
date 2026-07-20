# CallTrackingMetrics: Native API Reference

A consolidated summary of CallTrackingMetrics's API configuration and 23 documented operations, with links to official documentation.

- **Official docs:** https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/documentation/0ygaqwq/ctm-api
- **API base URL:** `https://api.calltrackingmetrics.com/api/v1`

## Authentication

### Basic Authentication

Connect CallTrackingMetrics with an access key and secret key.

### Credentials

- **Username:** `username` · required
- **Password:** `password` · required
- **Account ID:** `accountId` · required · The numeric CallTrackingMetrics account ID to use for account-scoped API requests.

Join the username and password with a colon, Base64-encode the result, and send it with the `Basic` authorization scheme:

```js
const credentials = Buffer.from(`${username}:${password}`).toString('base64');

const response = await fetch(url, {
  headers: {
    Authorization: `Basic ${credentials}`
  }
});
```

[Official authentication documentation](https://github.com/calltrackingmetrics/call-tracking-metrics-api/blob/master/getting-started.md)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (23 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Tracking Source](actions/create-tracking-source.md) | `POST /accounts/:accountId/sources.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/ri0maho/update-a-tracking-source) |
| [Create Webhook](actions/create-webhook.md) | `POST /accounts/:accountId/webhooks` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/0fgjrv6/create-webhook) |
| [Delete Tracking Source](actions/delete-tracking-source.md) | `DELETE /accounts/:accountId/sources/:sourceId.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/fhob7m4/list-of-tracking-sources) |
| [Delete Webhook](actions/delete-webhook.md) | `DELETE /accounts/:accountId/webhooks/:webhookId` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/ktu88w2/delete-webhook) |
| [Get Agency Information](actions/get-agency-information.md) | `GET /agency.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/yo3mrw8/agency-information) |
| [Get Agent Events](actions/get-agent-events.md) | `GET /accounts/:accountId/agents/events.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/e4cd4dd/agent-events) |
| [Get Call Setting Details](actions/get-call-setting-details.md) | `GET /accounts/:accountId/call_settings/:callSettingId.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/70ot7jk/list-details-of-a-call-setting) |
| [Get Tracking Source Details](actions/get-tracking-source-details.md) | `GET /accounts/:accountId/sources/:sourceId.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/c9snusb/delete-a-tracking-source) |
| [Get User Details](actions/get-user-details.md) | `GET /accounts/:accountId/users/:userId.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/64saoo4/user-details) |
| [Get Webhook Details](actions/get-webhook-details.md) | `GET /accounts/:accountId/webhooks/:webhookId` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/v9or8sj/webhook-details) |
| [List Accounts](actions/list-accounts.md) | `GET /accounts.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/0ygaqwq/ctm-api/list-of-accounts) |
| [List Active Account IDs And Names](actions/list-active-account-ids-and-names.md) | `GET /accounts.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/s1xvu1l/list-of-active-account-ids-and-names) |
| [List Activities](actions/list-activities.md) | `GET /accounts/:accountId/calls.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/uzx7unw/list-of-activities-calls-texts-chats-forms) |
| [List Call Setting Number Assignments](actions/list-call-setting-number-assignments.md) | `GET /accounts/:accountId/numbers.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/dg3mps1/list-of-numbers-assigned-and-available-to-assign-to-a-call-setting) |
| [List Call Settings](actions/list-call-settings.md) | `GET /accounts/:accountId/call_settings.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/oo7uk5g/set-default-call-setting) |
| [List Tracking Sources](actions/list-tracking-sources.md) | `GET /accounts/:accountId/sources.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/p7vym5s/tracking-source-details) |
| [List Users](actions/list-users.md) | `GET /accounts/:accountId/users.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/emrginr/list-of-users) |
| [List Webhooks](actions/list-webhooks.md) | `GET /accounts/:accountId/webhooks` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/b989srn/list-of-webhooks) |
| [Lookup Objects](actions/lookup-objects.md) | `GET /accounts/:accountId/lookup.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/7t5mc6u/lookup-api) |
| [Set Default Call Setting](actions/set-default-call-setting.md) | `PATCH /accounts/:accountId/call_settings/:callSettingId/set_default` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/t1mhehd/list-of-call-settings) |
| [Update Call Setting](actions/update-call-setting.md) | `PUT /accounts/:accountId/call_settings/:callSettingId.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/ebpj2uv/update-call-setting) |
| [Update Tracking Source](actions/update-tracking-source.md) | `PUT /accounts/:accountId/sources/:sourceId.json` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/ehkp4cj/create-new-tracking-source) |
| [Update Webhook](actions/update-webhook.md) | `PUT /accounts/:accountId/webhooks/:webhookId` | [docs](https://www.postman.com/ctm-8695/calltrackingmetrics-s-public-workspace/request/7e7u819/update-webhook) |
