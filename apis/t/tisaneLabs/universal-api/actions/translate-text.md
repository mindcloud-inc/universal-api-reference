# Tisane Labs: Translate Text

Translates input text in Tisane Labs.

```
GET https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/translate-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tisane Labs `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/translate-text?connectionId=$CONNECTION_ID&from=en&to=es&content=Hello%20world" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "en",
  "to": "es",
  "content": "Hello world"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tisaneLabs/latest/actions/translate-text?${params}`, {
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
| `from` | string | yes | IETF tag for the source language, or * / a vertical-bar-delimited set for autodetect. Example: `en`. |
| `to` | string | yes | IETF tag for the target language. Example: `es`. |
| `content` | string | yes | Text content to translate or paraphrase. Example: `Hello world`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `settings` | object | no | Optional translation settings object. Example: `[object Object]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Translated or paraphrased text. |

## Native endpoint

Through the native Tisane Labs API, this operation is `POST /transform` (base URL `https://api.tisane.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/translate-text.md) for the provider-specific parameters and requirements.

