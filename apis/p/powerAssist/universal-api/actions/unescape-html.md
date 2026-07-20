# Power Assist: Unescape HTML

Unescapes HTML entities with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/unescape-html
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/unescape-html?connectionId=$CONNECTION_ID&string=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "string": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/unescape-html?${params}`, {
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
| `string` | string | yes | The string containing HTML entities to unescape. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | string | Unescaped HTML result. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/string/unescapeHtml` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unescape-html.md) for the provider-specific parameters and requirements.

