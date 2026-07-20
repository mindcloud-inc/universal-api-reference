# Power Assist: Replace Text With Regex

Replaces text by regex in Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/replace-text-with-regex
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/replace-text-with-regex?connectionId=$CONNECTION_ID&sourceString=string&pattern=string&replaceValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceString": "string",
  "pattern": "string",
  "replaceValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/replace-text-with-regex?${params}`, {
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
| `sourceString` | string | yes | The string to search within. |
| `pattern` | string | yes | Regex pattern with leading and trailing slash, optionally followed by flags, for example /\\d+/gi. |
| `replaceValue` | string | yes | Replacement value to insert for each match. |

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
| `Result` | string | Regex replacement result. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/string/regexReplace` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-text-with-regex.md) for the provider-specific parameters and requirements.

