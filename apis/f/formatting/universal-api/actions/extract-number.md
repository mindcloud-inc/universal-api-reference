# Formatting: Extract Number

Extracts a number in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/extract-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/extract-number?connectionId=$CONNECTION_ID&input=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/extract-number?${params}`, {
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
| `input` | string | yes | The text to inspect for a number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "number": 1,
      "rawMatch": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `number` | number |  |
| `rawMatch` | string |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extract-number.md) for the provider-specific parameters and requirements.

