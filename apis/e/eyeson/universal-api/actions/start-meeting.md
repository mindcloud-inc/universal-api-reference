# Eyeson: Start Meeting



```
POST https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/start-meeting
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eyeson `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/start-meeting" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/start-meeting', {
  method: 'POST',
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eyeson API returns.

## Native endpoint

Through the native Eyeson API, this operation is `POST /rooms` (base URL `https://api.eyeson.team`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-meeting.md) for the provider-specific parameters and requirements.

