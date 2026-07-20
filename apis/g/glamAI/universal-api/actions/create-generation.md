# Glam AI: Create Generation

Creates an image generation in Glam AI.

```
POST https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/create-generation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Glam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/create-generation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mediaUrl": "https://example.com",
  "filterName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/create-generation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mediaUrl": "https://example.com",
    "filterName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaUrl` | string | yes | URL of the image or video to transform. |
| `filterName` | string | yes | Glam AI filter name, such as beetlejuice. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "event_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `event_id` | string | Generation event ID used to poll the result. |

## Native endpoint

Through the native Glam AI API, this operation is `POST /generate` (base URL `https://api.glam.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-generation.md) for the provider-specific parameters and requirements.

