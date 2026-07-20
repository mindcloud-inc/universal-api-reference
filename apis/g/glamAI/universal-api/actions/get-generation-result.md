# Glam AI: Get Generation Result

Retrieves an image generation result from Glam AI.

```
GET https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/get-generation-result
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Glam AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/get-generation-result?connectionId=$CONNECTION_ID&eventId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/glamAI/latest/actions/get-generation-result?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | yes | Generation event ID returned by Create Generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "media_urls": [
        "https://example.com"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `media_urls` | array<string> | Generated media URLs when ready. |
| `status` | string | Generation status. |

## Native endpoint

Through the native Glam AI API, this operation is `GET /result/:event_id` (base URL `https://api.glam.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-generation-result.md) for the provider-specific parameters and requirements.

