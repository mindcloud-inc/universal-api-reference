# Gainium: List Grid Backtest Requests



```
GET https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-grid-backtest-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Gainium `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-grid-backtest-requests?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gainium/latest/actions/list-grid-backtest-requests?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Field selection preset or custom field list. |
| `page` | number | no | 1-based page number. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Gainium API returns.

## Native endpoint

Through the native Gainium API, this operation is `GET /api/v2/backtest/grid/requests` (base URL `https://api.gainium.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-grid-backtest-requests.md) for the provider-specific parameters and requirements.

