# JoggAI: Generate AI Scripts



```
POST https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/generate-ai-scripts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a JoggAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/generate-ai-scripts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "language": "string",
  "product_info.source_type": "string",
  "scriptStyle": "string",
  "videoLengthSeconds": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/joggAI/latest/actions/generate-ai-scripts', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "language": "string",
    "product_info.source_type": "string",
    "scriptStyle": "string",
    "videoLengthSeconds": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language` | string | yes | Script language such as english or spanish |
| `product_info.data.description` | string | no | Product description when source type is details |
| `product_info.data.id` | string | no | Existing product ID when source type is id |
| `product_info.data.name` | string | no | Product name when source type is details |
| `product_info.source_type` | string | yes | Use id for an existing product or details for manual product details |
| `scriptStyle` | string | yes | Requested script style |
| `targetAudience` | string | no | Optional target audience description |
| `videoLengthSeconds` | string | yes | Desired video length in seconds: 15, 30, or 60 |

## Response

```json
{
  "success": true,
  "data": [
    {
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `taskId` | string | AI script generation task identifier |

## Native endpoint

Through the native JoggAI API, this operation is `POST /v2/ai_scripts` (base URL `https://api.jogg.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-ai-scripts.md) for the provider-specific parameters and requirements.

