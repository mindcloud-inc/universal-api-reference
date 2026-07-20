# WebCategorize: Categorize Content



```
POST https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/categorize-content
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebCategorize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/categorize-content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/categorize-content', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "html": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `html` | string | yes | Plain text or HTML content to categorize. |
| `url` | string | no | Optional URL stored for reference; it is not used for classification. |
| `tags[]` | array<string> | no | Optional tags to store with the content submission. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "feedback": {},
      "id": "string",
      "language": "string",
      "model": 1,
      "predictions": [
        {
          "confidence": "string",
          "id": "string",
          "name": "Ava Chen",
          "score": 1
        }
      ],
      "snippet": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contentType` | string | Detected content type. |
| `createdAt` | date | Categorization creation timestamp. |
| `feedback` | object | Feedback object, when available. |
| `id` | string | Content submission ID. |
| `language` | string | Detected language code. |
| `model` | number | Machine-learning model number used for detection. |
| `predictions` | array<object> | Predicted categories. |
| `predictions[].confidence` | string | Prediction confidence bucket. |
| `predictions[].id` | string | Predicted category ID. |
| `predictions[].name` | string | Predicted category name. |
| `predictions[].score` | number | Prediction confidence score. |
| `snippet` | string | Sample of the submitted content. |
| `status` | string | Categorization status. |
| `tags` | array<string> | Tags supplied by the user. |
| `url` | string | Reference URL supplied with the content. |

## Native endpoint

Through the native WebCategorize API, this operation is `POST /html` (base URL `https://app.webcategorize.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/categorize-content.md) for the provider-specific parameters and requirements.

