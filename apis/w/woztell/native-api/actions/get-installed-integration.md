# Get Installed Integration with Woztell

Retrieves an installed integration from your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [Get Installed Integration](https://doc.woztell.com/docs/reference/open-api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Optional GraphQL variables object. Supported keys include integrationId, build, and appIntegrationId. |
