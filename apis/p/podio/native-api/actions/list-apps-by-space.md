# List Apps by Space with Podio

Retrieves apps in a Podio space.

## Endpoint

- **Method:** `GET`
- **Path:** `/app/space/:space_id/`
- **Base URL:** `https://api.podio.com`
- **Official documentation:** [List Apps by Space](https://developers.podio.com/doc/applications/get-apps-by-space-22478)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `space_id` | path | `number` | yes | The space ID. |
| `include_inactive` | query | `boolean` | no | True if inactive apps should be included. |
