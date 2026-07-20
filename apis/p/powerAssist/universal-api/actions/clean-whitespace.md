# Power Assist: Clean Whitespace

Cleans whitespace in a string with Power Assist.

```
GET https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/clean-whitespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Power Assist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/clean-whitespace?connectionId=$CONNECTION_ID&string=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "string": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/powerAssist/latest/actions/clean-whitespace?${params}`, {
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
| `string` | string | yes | The string to clean. |

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
| `Result` | string | Cleaned string result. |

## Native endpoint

Through the native Power Assist API, this operation is `POST /api/string/clean` (base URL `https://power-assist.p.rapidapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clean-whitespace.md) for the provider-specific parameters and requirements.

