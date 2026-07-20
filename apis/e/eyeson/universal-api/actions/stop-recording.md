# Eyeson: Stop Recording



```
PUT https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/stop-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Eyeson `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/stop-recording" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eyeson/latest/actions/stop-recording', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessKey` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Eyeson API returns.

## Native endpoint

Through the native Eyeson API, this operation is `DELETE /rooms/:accessKey/recording` (base URL `https://api.eyeson.team`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/stop-recording.md) for the provider-specific parameters and requirements.

