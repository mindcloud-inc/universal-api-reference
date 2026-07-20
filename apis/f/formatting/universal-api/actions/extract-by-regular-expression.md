# Formatting: Extract by Regular Expression

Extracts text by regular expression in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/extract-by-regular-expression
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/extract-by-regular-expression?connectionId=$CONNECTION_ID&input=string&regExpString=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string",
  "regExpString": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/extract-by-regular-expression?${params}`, {
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
| `input` | string | yes | The text to search. |
| `regExpString` | string | yes | The regular expression pattern. |
| `flags` | string | no | The regex flags to apply. Default: `g`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "firstMatch": "string",
      "matches": [
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
| `firstMatch` | string |  |
| `matches` | array<string> |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-by-regular-expression.md) for the provider-specific parameters and requirements.

