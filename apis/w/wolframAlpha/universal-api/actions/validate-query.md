# Wolfram Alpha: Validate Query

Validates whether a Wolfram Alpha query can be processed.

```
GET https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/validate-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wolfram Alpha `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/validate-query?connectionId=$CONNECTION_ID&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wolframAlpha/latest/actions/validate-query?${params}`, {
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
| `input` | string | yes | Natural-language query to validate before requesting full results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "query": "string",
      "valid": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Validation message or diagnostics. |
| `query` | string | Original query text. |
| `valid` | boolean | Whether the query validated successfully. |

## Native endpoint

Through the native Wolfram Alpha API, this operation is `GET /v2/validatequery` (base URL `https://api.wolframalpha.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-query.md) for the provider-specific parameters and requirements.

