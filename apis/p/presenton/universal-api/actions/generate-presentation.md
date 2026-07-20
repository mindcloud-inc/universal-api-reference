# Presenton: Generate Presentation



```
POST https://connect.mindcloud.co/v1/universal/presenton/latest/actions/generate-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Presenton `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/presenton/latest/actions/generate-presentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "content": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/presenton/latest/actions/generate-presentation', {
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
| `content` | string | yes | Prompt or source content for the presentation. |
| `nSlides` | number | no | Number of slides to generate. |
| `template` | string | no | Template ID such as general. |
| `exportAs` | string | no | Export format such as pptx or pdf. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creditsConsumed": 1,
      "editPath": "string",
      "path": "string",
      "presentationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creditsConsumed` | number |  |
| `editPath` | string |  |
| `path` | string |  |
| `presentationId` | string |  |

## Native endpoint

Through the native Presenton API, this operation is `POST /api/v1/ppt/presentation/generate` (base URL `https://api.presenton.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-presentation.md) for the provider-specific parameters and requirements.

