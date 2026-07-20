# Dashcam: Publish Replay

Publishes a replay in Dashcam.

```
PUT https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/publish-replay
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashcam `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/publish-replay" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashcam/latest/actions/publish-replay', {
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
| `id` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dashcam API returns.

## Native endpoint

Through the native Dashcam API, this operation is `POST /api/v1/replay/publish` (base URL `https://api.testdriver.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-replay.md) for the provider-specific parameters and requirements.

