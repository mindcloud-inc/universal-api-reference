# WebCategorize: Retrieve URL Categorization



```
GET https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/retrieve-url-categorization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WebCategorize `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/retrieve-url-categorization?connectionId=$CONNECTION_ID&urlId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "urlId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webCategorize/latest/actions/retrieve-url-categorization?${params}`, {
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
| `urlId` | string | yes | The ID of the URL submission. |

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

Through the native WebCategorize API, this operation is `GET /url/{urlId}` (base URL `https://app.webcategorize.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-url-categorization.md) for the provider-specific parameters and requirements.

