# api4ai: Recognize Wine

Recognizes wine labels from an image URL in api4ai.

```
GET https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/recognize-wine
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a api4ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/recognize-wine?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/api4ai/latest/actions/recognize-wine?${params}`, {
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
| `url` | string | yes | Publicly reachable image URL to analyze. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "entities": {
          "classes": {}
        },
        "md5": "string",
        "name": "Ava Chen",
        "status": {
          "code": "string",
          "message": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | array<object> | Classification results. |
| `results.entities.classes` | object | Predicted classes and confidence scores. |
| `results.md5` | string | Processed image content hash. |
| `results.name` | string | Processed image name. |
| `results.status.code` | string | Processing status code. |
| `results.status.message` | string | Processing status message. |

## Native endpoint

Through the native api4ai API, this operation is `POST /wine-rec/v1/results` (base URL `https://api4ai.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recognize-wine.md) for the provider-specific parameters and requirements.

