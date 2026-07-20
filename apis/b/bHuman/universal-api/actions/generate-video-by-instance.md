# BHuman: Generate Video by Instance

Creates personalized videos from a video instance in BHuman.

```
POST https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/generate-video-by-instance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BHuman `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/generate-video-by-instance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoInstanceId": "string",
  "namesJson": "Ava Chen",
  "variablesJson": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bHuman/latest/actions/generate-video-by-instance', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoInstanceId": "string",
    "namesJson": "Ava Chen",
    "variablesJson": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetsJson` | string | no | Optional JSON string for the assets matrix. |
| `backgroundsJson` | string | no | Optional JSON string for the backgrounds array. |
| `callbackUrl` | string | no | Optional callback URL for async delivery. |
| `videoInstanceId` | string | yes | The video instance ID to generate from. |
| `namesJson` | string | yes | JSON string for the required nested names array. |
| `variablesJson` | string | yes | JSON string for the required variables array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native BHuman API returns.

## Native endpoint

Through the native BHuman API, this operation is `POST /ai_studio/try_sample` (base URL `https://studio.bhuman.ai/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-video-by-instance.md) for the provider-specific parameters and requirements.

