# Presenton: Generate Presentation Outlines V3



```
POST https://connect.mindcloud.co/v1/universal/presenton/latest/actions/generate-presentation-outlines-v3
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/generate-presentation-outlines-v3" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/presenton/latest/actions/generate-presentation-outlines-v3', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "content": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | yes | Prompt or source content for the outline. |
| `nSlides` | number | no | Number of slides to outline. |
| `includeTitleSlide` | boolean | no | Whether to include a title slide. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items[]` | array<string> |  |

## Native endpoint

Through the native Presenton API, this operation is `POST /api/v3/presentation/outlines/generate` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-presentation-outlines-v3.md) for the provider-specific parameters and requirements.

