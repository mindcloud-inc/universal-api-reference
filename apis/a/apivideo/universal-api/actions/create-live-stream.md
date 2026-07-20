# api.video: Create live stream

Creates a new live stream in api.video.

```
POST https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/create-live-stream
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a api.video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/create-live-stream" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apivideo/latest/actions/create-live-stream', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Optional display name for the live stream. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native api.video API returns.

## Native endpoint

Through the native api.video API, this operation is `POST /live-streams` (base URL `https://ws.api.video`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-live-stream.md) for the provider-specific parameters and requirements.

