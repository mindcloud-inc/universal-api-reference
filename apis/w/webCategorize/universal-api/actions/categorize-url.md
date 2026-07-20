# WebCategorize: Categorize URL



```
POST https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/categorize-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebCategorize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/categorize-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/categorize-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | URL to fetch and categorize. |
| `tags[]` | array<string> | no | Optional tags to store with the URL submission. |
| `cache` | boolean | no | Set true to look for an existing categorization of this URL. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cached": true,
      "code": 1,
      "contentType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "domain": "string",
      "feedback": {},
      "finalUrl": "https://example.com",
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
| `cached` | boolean | Whether the result was retrieved from cache. |
| `code` | number | HTTP status code from the final page. |
| `contentType` | string | Detected content type. |
| `createdAt` | date | Categorization creation timestamp. |
| `domain` | string | Domain of the final URL. |
| `feedback` | object | Feedback object, when available. |
| `finalUrl` | string | Final URL after redirects. |
| `id` | string | URL submission ID. |
| `language` | string | Detected language code. |
| `model` | number | Machine-learning model number used for detection. |
| `predictions` | array<object> | Predicted categories. |
| `predictions[].confidence` | string | Prediction confidence bucket. |
| `predictions[].id` | string | Predicted category ID. |
| `predictions[].name` | string | Predicted category name. |
| `predictions[].score` | number | Prediction confidence score. |
| `snippet` | string | Sample of the fetched content. |
| `status` | string | Categorization status. |
| `tags` | array<string> | Tags supplied by the user. |
| `url` | string | Original URL submitted. |

## Native endpoint

Through the native WebCategorize API, this operation is `POST /url` (base URL `https://app.webcategorize.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/categorize-url.md) for the provider-specific parameters and requirements.

