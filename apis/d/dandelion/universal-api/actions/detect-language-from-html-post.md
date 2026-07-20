# Dandelion: Detect Language From HTML via HTTP POST

Retrieves detected languages from HTML in Dandelion via HTTP POST.

```
GET https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/detect-language-from-html-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dandelion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/detect-language-from-html-post?connectionId=$CONNECTION_ID&html=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "html": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dandelion/latest/actions/detect-language-from-html-post?${params}`, {
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
| `html` | string | yes | HTML to analyze. |
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
      "text": "string",
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
| `detectedLangs` | array<object> |  |
| `text` | string | Extracted main content when html is used. |
| `time` | number |  |
| `timestamp` | string |  |

## Native endpoint

Through the native Dandelion API, this operation is `POST /datatxt/li/v1` (base URL `https://api.dandelion.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/detect-language-from-html-post.md) for the provider-specific parameters and requirements.

