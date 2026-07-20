# Formatting: Convert JSON to String

Converts JSON to a string in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/convert-json-to-string
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/convert-json-to-string?connectionId=$CONNECTION_ID&input=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/convert-json-to-string?${params}`, {
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
| `input` | object | yes | The JSON value to stringify. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jsonString": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jsonString` | string |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-json-to-string.md) for the provider-specific parameters and requirements.

