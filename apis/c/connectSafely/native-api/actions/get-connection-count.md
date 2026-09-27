# Get exact connection count with ConnectSafely

Returns the connected account's EXACT total connection count via LinkedIn's connectionsSummary endpoint — the real number, not the "500+" value LinkedIn shows on profiles. This reflects the authenticated account's own connections (select which connected account with `accountId`); it cannot return another member's connection count.

## Endpoint

- **Method:** `GET`
- **Path:** `/analytics/connections/count`
- **Base URL:** `https://api.connectsafely.ai/linkedin`
- **Official documentation:** [Get exact connection count](https://connectsafely.ai/docs/api/linkedin-analytics/get-analytics-connections-count-get-connection-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountId` | query | `string` | no | LinkedIn account ID to use. If omitted, uses the default account. |

## Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | `boolean` |  |
| `accountId` | `string` | LinkedIn account ID used |
| `connectionCount` | `number` | Exact total number of connections (uncapped), or null if LinkedIn did not return a count |

### Example response

```json
{
  "success": true,
  "accountId": "696ce9e780e0483585e4e553",
  "connectionCount": 3754
}
```

## Error status codes

`401`, `500`. Bodies follow the shared `{ success, code, message }` error shape.
