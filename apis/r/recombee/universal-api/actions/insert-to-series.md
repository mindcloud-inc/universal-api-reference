# Recombee: Insert to Series

Adds items to a series in Recombee.

```
POST https://connect.mindcloud.co/v1/universal/recombee/latest/actions/insert-to-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recombee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/insert-to-series" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "item-123",
  "itemType": "item",
  "seriesId": "series-123",
  "time": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recombee/latest/actions/insert-to-series', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "item-123",
    "itemType": "item",
    "seriesId": "series-123",
    "time": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cascadeCreate` | string | no |  |
| `itemId` | string | yes | Example: `item-123`. |
| `itemType` | string | yes | Example: `item`. |
| `seriesId` | string | yes | Example: `series-123`. |
| `time` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Recombee API returns.

## Native endpoint

Through the native Recombee API, this operation is `POST /series/:seriesId/items/` (base URL `https://rapi.recombee.com/{{credentials.databaseId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/insert-to-series.md) for the provider-specific parameters and requirements.

