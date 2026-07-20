# Power Assist: Replace All Text

Replaces all matching text with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/replace-all-text
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/replace-all-text?connectionId=$CONNECTION_ID&sourceString=string&searchValue=string&replaceValue=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sourceString": "string",
  "searchValue": "string",
  "replaceValue": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/replace-all-text?${params}`, {
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
| `searchValue` | string | yes | Case-sensitive substring to replace. |
| `replaceValue` | string | yes | Replacement value. |

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
| `Result` | string | Text replacement result. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/string/replaceAll` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-all-text.md) for the provider-specific parameters and requirements.

