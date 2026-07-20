# Apideck: Native API Reference

A consolidated summary of Apideck's API configuration and 33 documented operations, with links to official documentation.

- **Official docs:** https://developers.apideck.com/apis/vault/reference
- **OpenAPI specification:** https://specs.apideck.com/vault.yml
- **API base URL:** `https://unify.apideck.com`

## Authentication

### Custom Header Auth

Provide your Apideck Application ID and API Key. Requests send x-apideck-app-id plus Authorization: Bearer <API Key>.

### Credentials

- **Application Id:** `applicationId` · required · Your Apideck application ID used in the x-apideck-app-id header.
- **API Key:** `apiKey` · required · Your Apideck secret API key used in the Authorization bearer header.
- **Default Consumer Id:** `consumerId` · optional · Optional default x-apideck-consumer-id value for actions that require a consumer context.

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
x-apideck-app-id: <applicationId>
x-apideck-consumer-id: <consumerId>
```

[Official authentication documentation](https://developers.apideck.com/apis/vault/reference)

## API conventions

Responses from this API use JSON. Response data is read from `data`. The next-page cursor is read from `meta.cursors.next`.

## Pagination

Use `limit` in the query string to set the page size (default 20; accepted range 1–200). Use `cursor` in the query string as the pagination cursor.

## Retry behavior

Retry responses with status codes `429,500,502,503,504`. Wait 1000 ms before the first retry. Stop after 3 attempts. Multiply the delay by 2 after each failed attempt.

## Endpoints (33 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get consent records](actions/connectionconsentsall.md) | `GET /vault/connections/:unified_api/:service_id/consent` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Update consent state](actions/connectionconsentupdate.md) | `PATCH /vault/connections/:unified_api/:service_id/consent` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [List connection custom mappings](actions/connectioncustommappingsall.md) | `GET /vault/connections/:unified_api/:service_id/:resource/custom-mappings` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Create connection](actions/connectionsadd.md) | `POST /vault/connections/:unified_api/:service_id` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Get all connections](actions/connectionsall.md) | `GET /vault/connections` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Authorize](actions/connectionsauthorize.md) | `GET /vault/authorize/:service_id/:application_id` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Callback](actions/connectionscallback.md) | `GET /vault/callback` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Delete connection](actions/connectionsdelete.md) | `DELETE /vault/connections/:unified_api/:service_id` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Get resource settings](actions/connectionsettingsall.md) | `GET /vault/connections/:unified_api/:service_id/:resource/config` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Update settings](actions/connectionsettingsupdate.md) | `PATCH /vault/connections/:unified_api/:service_id/:resource/config` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Get resource example](actions/connectionsexample.md) | `GET /vault/connections/:unified_api/:service_id/:resource/example` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Import connection](actions/connectionsimport.md) | `POST /vault/connections/:unified_api/:service_id/import` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Get connection](actions/connectionsone.md) | `GET /vault/connections/:unified_api/:service_id` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Revoke connection](actions/connectionsrevoke.md) | `GET /vault/revoke/:service_id/:application_id` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Get resource schema](actions/connectionsschema.md) | `GET /vault/connections/:unified_api/:service_id/:resource/schema` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Authorize Access Token](actions/connectionstoken.md) | `POST /vault/connections/:unified_api/:service_id/token` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Update connection](actions/connectionsupdate.md) | `PATCH /vault/connections/:unified_api/:service_id` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Consumer request counts](actions/consumerrequestcountsall.md) | `GET /vault/consumers/:consumer_id/stats` | [docs](https://developers.apideck.com/apis/vault/reference/consumers) |
| [Create consumer](actions/consumersadd.md) | `POST /vault/consumers` | [docs](https://developers.apideck.com/apis/vault/reference/consumers) |
| [Get all consumers](actions/consumersall.md) | `GET /vault/consumers` | [docs](https://developers.apideck.com/apis/vault/reference/consumers) |
| [Delete consumer](actions/consumersdelete.md) | `DELETE /vault/consumers/:consumer_id` | [docs](https://developers.apideck.com/apis/vault/reference/consumers) |
| [Get consumer](actions/consumersone.md) | `GET /vault/consumers/:consumer_id` | [docs](https://developers.apideck.com/apis/vault/reference/consumers) |
| [Update consumer](actions/consumersupdate.md) | `PATCH /vault/consumers/:consumer_id` | [docs](https://developers.apideck.com/apis/vault/reference/consumers) |
| [Create Callback State](actions/createcallbackstate.md) | `POST /vault/connections/:unified_api/:service_id/callback-state` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Get resource custom fields](actions/customfieldsall.md) | `GET /vault/connections/:unified_api/:service_id/:resource/custom-fields` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
| [Create custom mapping](actions/custommappingsadd.md) | `POST /vault/custom-mappings/:unified_api/:service_id/:target_field_id` | [docs](https://developers.apideck.com/apis/vault/reference/custom-mappings) |
| [List custom mappings](actions/custommappingsall.md) | `GET /vault/custom-mappings/:unified_api/:service_id` | [docs](https://developers.apideck.com/apis/vault/reference/custom-mappings) |
| [Delete custom mapping](actions/custommappingsdelete.md) | `DELETE /vault/custom-mappings/:unified_api/:service_id/:target_field_id` | [docs](https://developers.apideck.com/apis/vault/reference/custom-mappings) |
| [Get custom mapping](actions/custommappingsone.md) | `GET /vault/custom-mappings/:unified_api/:service_id/:target_field_id` | [docs](https://developers.apideck.com/apis/vault/reference/custom-mappings) |
| [Update custom mapping](actions/custommappingsupdate.md) | `PATCH /vault/custom-mappings/:unified_api/:service_id/:target_field_id` | [docs](https://developers.apideck.com/apis/vault/reference/custom-mappings) |
| [Get all consumer request logs](actions/logsall.md) | `GET /vault/logs` | [docs](https://developers.apideck.com/apis/vault/reference) |
| [Create session](actions/sessionscreate.md) | `POST /vault/sessions` | [docs](https://developers.apideck.com/apis/vault/reference) |
| [Validate Connection State](actions/validateconnectionstate.md) | `POST /vault/connections/:unified_api/:service_id/validate` | [docs](https://developers.apideck.com/apis/vault/reference/connections) |
