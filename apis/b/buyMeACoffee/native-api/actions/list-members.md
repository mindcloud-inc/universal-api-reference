# List Members with Buy Me a Coffee

Retrieves members from Buy Me a Coffee.

## Endpoint

- **Method:** `GET`
- **Path:** `/subscriptions`
- **Base URL:** `https://developers.buymeacoffee.com/api/v1`
- **Official documentation:** [List Members](https://developers.buymeacoffee.com/apireference.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status` | query | `string` | yes | Filter memberships by status. Official docs allow active, inactive, or all. |
