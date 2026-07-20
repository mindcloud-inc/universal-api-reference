# List Actions with Pingdom

## Endpoint

- **Method:** `GET`
- **Path:** `/actions`
- **Base URL:** `https://api.pingdom.com/api/3.1`
- **Official documentation:** [List Actions](https://docs.pingdom.com/api/#tag/Actions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `from` | query | `number` | no | Only include actions generated later than this UNIX timestamp. |
| `to` | query | `number` | no | Only include actions generated earlier than this UNIX timestamp. |
| `checkids` | query | `string` | no | Comma-separated list of check identifiers to filter actions. |
| `userids` | query | `string` | no | Comma-separated list of user identifiers to filter actions. |
| `status` | query | `string` | no | Comma-separated list of action statuses to include. |
| `via` | query | `string` | no | Comma-separated list of delivery mediums to include. |
