# Get Item with Qlik

Retrieves an item from your Qlik tenant.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/items/:itemId`
- **Base URL:** `https://{tenantHost}`
- **Official documentation:** [Get Item](https://qlik.dev/apis/rest/items/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `itemId` | path | `string` | yes | Qlik item ID. |
