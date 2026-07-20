# Dandelion: Detect Language From Text via HTTP POST

Retrieves detected languages from text in Dandelion via HTTP POST.

```
GET https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/detect-language-from-text-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dandelion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/detect-language-from-text-post?connectionId=$CONNECTION_ID&text=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "text": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/detect-language-from-text-post?${params}`, {
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
| `text` | string | yes | Text to analyze. |
| `clean` | boolean | no | Clean URLs, email addresses, hashtags, and more before analysis. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detectedLangs": [
        {}
      ],
      "time": 1,
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `detectedLangs` | array<object> | Detected languages ordered by confidence. |
| `time` | number | Elapsed time in milliseconds. |
| `timestamp` | string | Response generation timestamp. |

## Native endpoint

Through the native Dandelion API, this operation is `POST /datatxt/li/v1` (base URL `https://api.dandelion.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-language-from-text-post.md) for the provider-specific parameters and requirements.

