# Reka AI: Plan Features

Creates a feature plan in Reka AI.

```
POST https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/plan-features
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/plan-features" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "desired": "string",
  "video_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/plan-features', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "desired": "string",
    "video_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `desired` | string | yes | Desired features to plan |
| `video_id` | string | yes | The video identifier to plan features for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Primary identifier. |
| `message` | string | Human-readable message. |
| `status` | string | Current status. |

## Native endpoint

Through the native Reka AI API, this operation is `POST https://vision-agent.api.reka.ai/v2/videos/:video_id/features/plan` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/plan-features.md) for the provider-specific parameters and requirements.

