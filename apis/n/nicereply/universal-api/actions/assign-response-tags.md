# Nicereply: Assign Response Tags

Assigns a tag to a response in Nicereply.

```
PUT https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/assign-response-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nicereply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/assign-response-tags" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nicereply/latest/actions/assign-response-tags', {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nicereply API returns.

## Native endpoint

Through the native Nicereply API, this operation is `POST /responses/:responseId/tags/:tagId` (base URL `https://api.nicereply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-response-tags.md) for the provider-specific parameters and requirements.

