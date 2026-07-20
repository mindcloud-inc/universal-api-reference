# Cancel scheduled SMS request with Webex Interact

Cancels a scheduled SMS request in Webex Interact.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/campaigns/v1/cancel/{id}`
- **Base URL:** `https://api.webexinteract.com`
- **Official documentation:** [Cancel scheduled SMS request](https://docs.webexinteract.com/reference/scheduled-messages-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Campaign or API SMS request ID to cancel. |
