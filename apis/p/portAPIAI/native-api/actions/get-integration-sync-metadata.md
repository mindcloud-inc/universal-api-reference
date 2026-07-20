# Get Integration Sync Metadata with Port API AI

Retrieves integration sync metadata from Port.

## Endpoint

- **Method:** `GET`
- **Path:** `/integration/:integrationInternalId/syncsMetadata`
- **Base URL:** `https://api.port.io/v1`
- **Official documentation:** [Get Integration Sync Metadata](https://docs.port.io/api-reference/get-an-integrations-sync-metadata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `integrationInternalId` | path | `string` | yes | The integration internal identifier. |
