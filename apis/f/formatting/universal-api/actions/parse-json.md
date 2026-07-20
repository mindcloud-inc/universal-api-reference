# Formatting: Parse JSON

Parses a JSON string in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/parse-json
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/parse-json?connectionId=$CONNECTION_ID&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/parse-json?${params}`, {
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
| `input` | string | yes | The JSON string to parse. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "parsedValue": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `parsedValue` | object |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-json.md) for the provider-specific parameters and requirements.

