# Intervals.icu: Update Wellness Records Bulk

Updates wellness records in Intervals.icu.

```
PUT https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/update-wellness-records-bulk
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Intervals.icu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/update-wellness-records-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/intervalsicu/latest/actions/update-wellness-records-bulk', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Intervals.icu API returns.

## Native endpoint

Through the native Intervals.icu API, this operation is `PUT /api/v1/athlete/:id/wellness-bulk` (base URL `https://intervals.icu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-wellness-records-bulk.md) for the provider-specific parameters and requirements.

