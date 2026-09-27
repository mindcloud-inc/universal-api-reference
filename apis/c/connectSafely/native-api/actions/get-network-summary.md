# Get "Manage my network" counts with ConnectSafely

Returns the connected account's own network counts as shown in the "Manage my network" card: connections, groups, events, pages and newsletters. The connection count here is the EXACT number, not the "500+" value LinkedIn shows on profiles. Read live from the my-network SDUI screen on every call (select which connected account with `accountId`); it cannot return another member's counts.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/network/summary`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get "Manage my network" counts](https://connectsafely.ai/docs/api/linkedin-analytics/get-analytics-network-summary-get-network-summary)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If omitted, uses the default account. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` | LinkedIn account ID used |
| `connections` | `number` | Exact total number of connections (uncapped) |
| `groups` | `number` | Groups the account belongs to |
| `events` | `number` | Events the account is attending |
| `pages` | `number` | Company pages the account follows |
| `newsletters` | `number` | Newsletters the account subscribes to |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "connections": 1419,
  "groups": 14,
  "events": 1,
  "pages": 17,
  "newsletters": 7
}
```

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
