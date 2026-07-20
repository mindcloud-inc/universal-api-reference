# Recombee: Add Series

Creates a new series in Recombee.

```
POST https://connect.mindcloud.co/v1/universal/recombee/latest/actions/add-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recombee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/recombee/latest/actions/add-series" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "seriesId": "series-123"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recombee/latest/actions/add-series', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "seriesId": "series-123"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cascadeCreate` | string | no |  |
| `seriesId` | string | yes | Example: `series-123`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Recombee API returns.

## Native endpoint

Through the native Recombee API, this operation is `PUT /series/:seriesId` (base URL `https://rapi.recombee.com/{{credentials.databaseId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-series.md) for the provider-specific parameters and requirements.

