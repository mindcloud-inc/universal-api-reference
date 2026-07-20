# Delete Connections with Pabbly Hook

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v1/connections`
- **Base URL:** `https://hook.pabbly.com`
- **Official documentation:** [Delete Connections](https://apidocs.pabbly.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `connection_ids[]` | body | `array<string>` | yes | Connection IDs to move to trash. |
