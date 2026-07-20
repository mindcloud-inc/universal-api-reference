# Wolfram Alpha: Recognize Query JSON

Recognizes a query in Wolfram Alpha and returns JSON.

```
GET https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/recognize-query-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wolfram Alpha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/recognize-query-json?connectionId=$CONNECTION_ID&i=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "i": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/recognize-query-json?${params}`, {
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
| `i` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formula": "string",
      "message": "string",
      "path": "string",
      "query": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formula` | string | Recognized formula or normalized expression. |
| `message` | string | Recognition message. |
| `path` | string | Recognized Wolfram path when available. |
| `query` | string | Original query text. |

## Native endpoint

Through the native Wolfram Alpha API, this operation is `GET https://www.wolframalpha.com/queryrecognizer/query.jsp` (base URL `https://api.wolframalpha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recognize-query-json.md) for the provider-specific parameters and requirements.

