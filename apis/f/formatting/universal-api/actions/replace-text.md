# Formatting: Replace Text

Replaces text in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/replace-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/replace-text?connectionId=$CONNECTION_ID&input=string&findText=string&replaceText=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string",
  "findText": "string",
  "replaceText": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/replace-text?${params}`, {
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
| `input` | string | yes | The source text. |
| `findText` | string | yes | The text or pattern to replace. |
| `replaceText` | string | yes | The replacement text. |
| `useRegex` | boolean | no | Whether to treat Find Text as a regular expression. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "replacedText": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `replacedText` | string |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-text.md) for the provider-specific parameters and requirements.

