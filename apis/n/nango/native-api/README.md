# Nango: Native API Reference

A consolidated summary of Nango's API configuration and 50 documented operations, with links to official documentation.

- **Official docs:** https://nango.dev/docs/reference/api/authentication
- **OpenAPI specification:** https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml
- **API base URL:** `https://api.nango.dev`

## Authentication

### Secret Key

Use the Nango secret key from Environment Settings. MindCloud injects it as Authorization: Bearer <secret-key>.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://nango.dev/docs/reference/api/authentication)

## API conventions

Response data is read from `data`.

## Endpoints (50 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Connect Session](actions/create-connect-session.md) | `POST /connect/sessions` | [docs](https://nango.dev/docs/reference/api/connect/sessions/create) |
| [Create Integration](actions/create-integration.md) | `POST /integrations` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
| [Create Integration (Config)](actions/create-integration-config.md) | `POST /config` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
| [Create Reconnect Session](actions/create-reconnect-session.md) | `POST /connect/sessions/reconnect` | [docs](https://docs.nango.dev/reference/api/connect/sessions/reconnect) |
| [Create Sync Variant](actions/create-sync-variant.md) | `POST /sync/:name/variant/:variant` | [docs](https://nango.dev/docs/reference/api/sync/create-variant) |
| [Delete Connect Session](actions/delete-connect-session.md) | `DELETE /connect/session` | [docs](https://docs.nango.dev/reference/api/connect/session/delete) |
| [Delete Connection](actions/delete-connection.md) | `DELETE /connections/:connectionId` | [docs](https://nango.dev/docs/reference/api/connections/delete) |
| [Delete Connection (Deprecated)](actions/delete-connection-deprecated.md) | `DELETE /connection/:connectionId` | [docs](https://nango.dev/docs/reference/api/connection/delete) |
| [Delete Integration](actions/delete-integration.md) | `DELETE /integrations/:providerConfigKey` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
| [Delete Integration (Config)](actions/delete-integration-config.md) | `DELETE /config/:providerConfigKey` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
| [Delete Sync Variant](actions/delete-sync-variant.md) | `DELETE /sync/:name/variant/:variant` | [docs](https://nango.dev/docs/reference/api/sync/delete-variant) |
| [Get Async Action Result](actions/get-async-action-result.md) | `GET /action/:actionId` | [docs](https://docs.nango.dev/implementation-guides/actions/async-actions) |
| [Get Connect Session](actions/get-connect-session.md) | `GET /connect/session` | [docs](https://docs.nango.dev/reference/api/connect/session/get) |
| [Get Connection](actions/get-connection.md) | `GET /connections/:connectionId` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
| [Get Connection With Credentials (Deprecated)](actions/get-connection-deprecated.md) | `GET /connection/:connectionId` | [docs](https://docs.nango.dev/reference/api/connection/get) |
| [Get Integration](actions/get-integration.md) | `GET /integrations/:providerConfigKey` | [docs](https://docs.nango.dev/reference/api/integration/get) |
| [Get Integration (Config)](actions/get-integration-config.md) | `GET /config/:providerConfigKey` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
| [Get Integration Functions Config](actions/get-integration-functions-config.md) | `GET /scripts/config` | [docs](https://nango.dev/docs/reference/api/scripts/config) |
| [Get Provider](actions/get-provider.md) | `GET /providers/:provider` | [docs](https://nango.dev/docs/reference/api/providers/get) |
| [Get Records](actions/get-records.md) | `GET /records` | [docs](https://docs.nango.dev/reference/api/records/get) |
| [Get Sync Records](actions/get-sync-records.md) | `GET /sync/records` | [docs](https://docs.nango.dev/reference/api/sync/records/get) |
| [Get Sync Status](actions/get-sync-status.md) | `GET /sync/status` | [docs](https://docs.nango.dev/reference/api/sync/status) |
| [Import Connection](actions/import-connection.md) | `POST /connections` | [docs](https://docs.nango.dev/reference/api/connections/post) |
| [Import Connection (Deprecated)](actions/import-connection-deprecated.md) | `POST /connection` | [docs](https://nango.dev/docs/reference/api/connection/post) |
| [List Connections](actions/list-connections.md) | `GET /connections` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
| [List Connections (Deprecated)](actions/list-connections-deprecated.md) | `GET /connection` | [docs](https://nango.dev/docs/reference/api/connection/list) |
| [List Environment Variables](actions/list-environment-variables.md) | `GET /environment-variables` | [docs](https://nango.dev/docs/reference/api/environment-variables/get) |
| [List Integrations](actions/list-integrations.md) | `GET /integrations` | [docs](https://nango.dev/docs/reference/api/integration/list) |
| [List Integrations (Config)](actions/list-integrations-config.md) | `GET /config` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
| [List Providers](actions/list-providers.md) | `GET /providers` | [docs](https://nango.dev/docs/reference/api/providers/get) |
| [Patch Connection](actions/patch-connection.md) | `PATCH /connections/:connectionId` | [docs](https://nango.dev/docs/reference/api/connections/patch) |
| [Pause Sync](actions/pause-sync.md) | `POST /sync/pause` | [docs](https://docs.nango.dev/reference/api/sync/pause) |
| [Proxy DELETE](actions/proxy-delete.md) | `DELETE /proxy/:anyPath` | [docs](https://docs.nango.dev/reference/api/proxy/delete) |
| [Proxy GET](actions/proxy-get.md) | `GET /proxy/:anyPath` | [docs](https://docs.nango.dev/reference/api/proxy/get) |
| [Proxy PATCH](actions/proxy-patch.md) | `PATCH /proxy/:anyPath` | [docs](https://docs.nango.dev/reference/api/proxy/patch) |
| [Proxy POST](actions/proxy-post.md) | `POST /proxy/:anyPath` | [docs](https://docs.nango.dev/reference/api/proxy/post) |
| [Proxy PUT](actions/proxy-put.md) | `PUT /proxy/:anyPath` | [docs](https://docs.nango.dev/reference/api/proxy/put) |
| [Prune Records](actions/prune-records.md) | `PATCH /records/prune` | [docs](https://nango.dev/docs/reference/api/sync/prune-records) |
| [Set Connection Metadata](actions/set-connection-metadata.md) | `POST /connection/:connectionId/metadata` | [docs](https://docs.nango.dev/reference/api/connection/metadata/post) |
| [Set Connection Metadata Bulk (Deprecated)](actions/set-connection-metadata-bulk-deprecated.md) | `POST /connection/metadata` | [docs](https://docs.nango.dev/reference/api/connection/set-metadata) |
| [Set Connections Metadata](actions/set-connections-metadata.md) | `POST /connections/metadata` | [docs](https://nango.dev/docs/reference/api/connections/set-metadata) |
| [Start Sync](actions/start-sync.md) | `POST /sync/start` | [docs](https://docs.nango.dev/reference/api/sync/start) |
| [Trigger Action](actions/trigger-action.md) | `POST /action/trigger` | [docs](https://docs.nango.dev/reference/api/action/trigger) |
| [Trigger Sync](actions/trigger-sync.md) | `POST /sync/trigger` | [docs](https://docs.nango.dev/reference/api/sync/trigger) |
| [Update Connection Frequency](actions/update-connection-frequency.md) | `PUT /sync/update-connection-frequency` | [docs](https://docs.nango.dev/reference/api/sync/update-connection-frequency) |
| [Update Connection Metadata](actions/update-connection-metadata.md) | `PATCH /connection/:connectionId/metadata` | [docs](https://docs.nango.dev/reference/api/connection/metadata/patch) |
| [Update Connection Metadata Bulk (Deprecated)](actions/update-connection-metadata-bulk-deprecated.md) | `PATCH /connection/metadata` | [docs](https://nango.dev/docs/reference/api/connection/update-metadata) |
| [Update Connections Metadata](actions/update-connections-metadata.md) | `PATCH /connections/metadata` | [docs](https://nango.dev/docs/reference/api/connections/update-metadata) |
| [Update Integration](actions/update-integration.md) | `PUT /integrations` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
| [Update Integration (Config)](actions/update-integration-config.md) | `PUT /config` | [docs](https://raw.githubusercontent.com/speakeasy-sdks/nango-typescript-sdk/main/openapi.yaml) |
