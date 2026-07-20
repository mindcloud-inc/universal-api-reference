# Alai: Generate Presentation

Creates an async presentation generation in Alai from text input.

```
POST https://connect.mindcloud.co/v1/universal/alai/latest/actions/generate-presentation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alai/latest/actions/generate-presentation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputText": "string",
  "presentationOptions.title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alai/latest/actions/generate-presentation', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputText": "string",
    "presentationOptions.title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputText` | string | yes | Source text used to generate the presentation. |
| `presentationOptions.title` | string | yes | Title for the generated presentation. |
| `presentationOptions.slideRange` | string | no | Requested slide count range like 2-3 or 6-10. Example: `2-3`. |
| `presentationOptions.themeId` | string | no | Theme identifier returned by Get Themes. |
| `exportFormats[]` | array<string> | no | Requested export formats like link, pdf, or ppt. |
| `imageIds[]` | array<string> | no | Uploaded image identifiers to include in generation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "generationId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `generationId` | string |  |

## Native endpoint

Through the native Alai API, this operation is `POST /generations` (base URL `https://slides-api.getalai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-presentation.md) for the provider-specific parameters and requirements.

