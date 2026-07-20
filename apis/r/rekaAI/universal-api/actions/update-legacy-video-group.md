# Reka AI: Update Legacy Video Group

Updates an existing legacy video group in Reka AI.

```
PUT https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/update-legacy-video-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/update-legacy-video-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "group_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/update-legacy-video-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "group_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `group_id` | string | yes | The legacy video group identifier to update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
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
| `name` | string | Display name. |
| `status` | string | Status value. |

## Native endpoint

Through the native Reka AI API, this operation is `PATCH https://vision-agent.api.reka.ai/v1/video-groups/:group_id` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-legacy-video-group.md) for the provider-specific parameters and requirements.

