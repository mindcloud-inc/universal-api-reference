# Shadify: Generate Multiplication Expression

Retrieves a random multiplication expression from Shadify.

```
GET https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-multiplication-expression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shadify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-multiplication-expression?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shadify/latest/actions/generate-multiplication-expression?${params}`, {
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
| `minFirst` | number | no | Optional minimum value for the first number. Default is 1. Default: `1`. |
| `maxFirst` | number | no | Optional maximum value for the first number. Default is 99. Default: `99`. |
| `minSecond` | number | no | Optional minimum value for the second number. Default is 1. Default: `1`. |
| `maxSecond` | number | no | Optional maximum value for the second number. Default is 99. Default: `99`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer": 1,
      "expression": "string",
      "first": 1,
      "operation": "string",
      "second": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer` | number | Correct answer. |
| `expression` | string | Expression text. |
| `first` | number | First operand. |
| `operation` | string | Math operator. |
| `second` | number | Second operand. |

## Native endpoint

Through the native Shadify API, this operation is `GET /math/mul` (base URL `https://shadify.yurace.pro/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-multiplication-expression.md) for the provider-specific parameters and requirements.

