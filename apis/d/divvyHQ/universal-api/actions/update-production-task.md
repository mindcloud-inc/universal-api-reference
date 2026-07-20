# DivvyHQ: Update Production Task



```
PUT https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/update-production-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DivvyHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/update-production-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/divvyHQ/latest/actions/update-production-task', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native DivvyHQ API returns.

## Native endpoint

Through the native DivvyHQ API, this operation is `PUT /productiontasks/:id/` (base URL `https://app.divvyhq.com/api/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-production-task.md) for the provider-specific parameters and requirements.

