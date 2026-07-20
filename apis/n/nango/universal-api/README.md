# <img src="https://images.mindcloud.co/apps/icons/nango-icon-square_1776264161637.png" alt="Nango logo" width="28" height="28"> Nango: Universal API

Use the Nango HTTP API to manage integrations, connections, syncs, actions, proxy calls, and environment data for a Nango workspace.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/nango/latest
- **Category:** IT Operations / Developer Tools
- **Actions:** 50
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.nango.dev
- **Vendor API docs:** https://nango.dev/docs/reference/api/authentication

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Integrations](actions/list-integrations.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nango/latest/actions/list-integrations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (50)

### Action

| Action | Method | Description |
| --- | --- | --- |
| [Trigger Action](actions/trigger-action.md) | POST |  |

### Action Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Async Action Result](actions/get-async-action-result.md) | GET |  |

### Connect Session

| Action | Method | Description |
| --- | --- | --- |
| [Create Connect Session](actions/create-connect-session.md) | POST |  |
| [Create Reconnect Session](actions/create-reconnect-session.md) | POST |  |
| [Delete Connect Session](actions/delete-connect-session.md) | DELETE |  |
| [Get Connect Session](actions/get-connect-session.md) | GET |  |

### Connection

| Action | Method | Description |
| --- | --- | --- |
| [Delete Connection (Deprecated)](actions/delete-connection-deprecated.md) | DELETE |  |
| [Get Connection With Credentials (Deprecated)](actions/get-connection-deprecated.md) | GET |  |
| [Import Connection (Deprecated)](actions/import-connection-deprecated.md) | POST |  |
| [List Connections (Deprecated)](actions/list-connections-deprecated.md) | GET |  |
| [Patch Connection](actions/patch-connection.md) | PUT |  |
| [Set Connection Metadata](actions/set-connection-metadata.md) | POST |  |
| [Set Connection Metadata Bulk (Deprecated)](actions/set-connection-metadata-bulk-deprecated.md) | POST |  |
| [Set Connections Metadata](actions/set-connections-metadata.md) | POST |  |
| [Update Connection Metadata](actions/update-connection-metadata.md) | PUT |  |
| [Update Connection Metadata Bulk (Deprecated)](actions/update-connection-metadata-bulk-deprecated.md) | PUT |  |
| [Update Connections Metadata](actions/update-connections-metadata.md) | PUT |  |

### Connections

| Action | Method | Description |
| --- | --- | --- |
| [Delete Connection](actions/delete-connection.md) | DELETE |  |
| [Get Connection](actions/get-connection.md) | GET |  |
| [Import Connection](actions/import-connection.md) | POST |  |
| [List Connections](actions/list-connections.md) | GET |  |

### Environment Variable

| Action | Method | Description |
| --- | --- | --- |
| [List Environment Variables](actions/list-environment-variables.md) | GET |  |

### Integration

| Action | Method | Description |
| --- | --- | --- |
| [Create Integration (Config)](actions/create-integration-config.md) | POST |  |
| [Delete Integration (Config)](actions/delete-integration-config.md) | DELETE |  |
| [Get Integration (Config)](actions/get-integration-config.md) | GET |  |
| [List Integrations (Config)](actions/list-integrations-config.md) | GET |  |
| [Update Integration (Config)](actions/update-integration-config.md) | PUT |  |

### Integration Functions Config

| Action | Method | Description |
| --- | --- | --- |
| [Get Integration Functions Config](actions/get-integration-functions-config.md) | GET |  |

### Integrations

| Action | Method | Description |
| --- | --- | --- |
| [Create Integration](actions/create-integration.md) | POST |  |
| [Delete Integration](actions/delete-integration.md) | DELETE |  |
| [Get Integration](actions/get-integration.md) | GET |  |
| [List Integrations](actions/list-integrations.md) | GET |  |
| [Update Integration](actions/update-integration.md) | PUT |  |

### Provider

| Action | Method | Description |
| --- | --- | --- |
| [Get Provider](actions/get-provider.md) | GET |  |
| [List Providers](actions/list-providers.md) | GET |  |

### Proxy Request

| Action | Method | Description |
| --- | --- | --- |
| [Proxy DELETE](actions/proxy-delete.md) | DELETE |  |
| [Proxy GET](actions/proxy-get.md) | GET |  |
| [Proxy PATCH](actions/proxy-patch.md) | PUT |  |
| [Proxy POST](actions/proxy-post.md) | POST |  |
| [Proxy PUT](actions/proxy-put.md) | PUT |  |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Records](actions/get-records.md) | GET |  |
| [Get Sync Records](actions/get-sync-records.md) | GET |  |
| [Prune Records](actions/prune-records.md) | PUT |  |

### Sync

| Action | Method | Description |
| --- | --- | --- |
| [Get Sync Status](actions/get-sync-status.md) | GET |  |
| [Pause Sync](actions/pause-sync.md) | PUT |  |
| [Start Sync](actions/start-sync.md) | POST |  |
| [Trigger Sync](actions/trigger-sync.md) | POST |  |
| [Update Connection Frequency](actions/update-connection-frequency.md) | PUT |  |

### Sync Variant

| Action | Method | Description |
| --- | --- | --- |
| [Create Sync Variant](actions/create-sync-variant.md) | POST |  |
| [Delete Sync Variant](actions/delete-sync-variant.md) | DELETE |  |

