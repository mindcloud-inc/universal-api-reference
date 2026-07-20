# Ayrshare: Translate Post

Translates a post in Ayrshare.

```
POST https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/translate-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/translate-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "text": "string",
  "lang": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/translate-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "text": "string",
    "lang": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `text` | string | yes | Text to translate. |
| `lang` | string | yes | ISO language code to translate text into, such as es or fr. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "language": "string",
      "message": "string",
      "originalText": "string",
      "status": "string",
      "translatedText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number | Ayrshare error code. |
| `language` | string | Target language code. |
| `message` | string | Translation or error message. |
| `originalText` | string | Original submitted text. |
| `status` | string | Translation status. |
| `translatedText` | string | Translated text. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /generate/translate` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-post.md) for the provider-specific parameters and requirements.

