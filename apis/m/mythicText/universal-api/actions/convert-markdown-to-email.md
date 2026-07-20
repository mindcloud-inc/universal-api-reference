# Mythic Text: Convert Markdown To Email



```
GET https://connect.mindcloud.co/v1/universal/mythicText/latest/actions/convert-markdown-to-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mythic Text `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mythicText/latest/actions/convert-markdown-to-email?connectionId=$CONNECTION_ID&markdown=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "markdown": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mythicText/latest/actions/convert-markdown-to-email?${params}`, {
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
| `markdown` | string | yes | Markdown content to convert to email output. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "html": "string",
      "model": "string",
      "processing_time_ms": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `html` | string | Converted output returned by Mythic Text. |
| `model` | string | Model identifier reported by Mythic Text. |
| `processing_time_ms` | number | Conversion time reported by Mythic Text in milliseconds. |

## Native endpoint

Through the native Mythic Text API, this operation is `POST /convert` (base URL `https://mythictext-api.vercel.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-markdown-to-email.md) for the provider-specific parameters and requirements.

