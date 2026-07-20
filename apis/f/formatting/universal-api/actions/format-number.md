# Formatting: Format Number

Formats a number in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/format-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/format-number?connectionId=$CONNECTION_ID&input=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/format-number?${params}`, {
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
| `input` | number | yes | The number to format. |
| `locale` | string | no | The locale to use for formatting. Default: `en-US`. |
| `maximumFractionDigits` | number | no | The maximum number of fraction digits. Default: `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formattedNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formattedNumber` | string |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/format-number.md) for the provider-specific parameters and requirements.

