# Power Assist: Count Words

Counts words in a string with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/count-words
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/count-words?connectionId=$CONNECTION_ID&string=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "string": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/count-words?${params}`, {
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
| `string` | string | yes | The string to count words in. |

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
      "Result": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Result` | number | Number of words. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/string/wordCount` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/count-words.md) for the provider-specific parameters and requirements.

