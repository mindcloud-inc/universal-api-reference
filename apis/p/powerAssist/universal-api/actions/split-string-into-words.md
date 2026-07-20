# Power Assist: Split String Into Words

Splits a string into words with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/split-string-into-words
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/split-string-into-words?connectionId=$CONNECTION_ID&string=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "string": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/split-string-into-words?${params}`, {
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
| `string` | string | yes | The string to split. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `delimiter` | string | no | Optional delimiter or regex pattern. Leave blank to split on whitespace. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Result": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | array<string> | Words extracted from the input string. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/string/words` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/split-string-into-words.md) for the provider-specific parameters and requirements.

