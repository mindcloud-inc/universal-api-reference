# Formatting: Format Currency

Formats currency in the Formatting app.

```
GET https://connect.mindcloud.co/v1/universal/formatting/latest/actions/format-currency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Formatting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/formatting/latest/actions/format-currency?connectionId=$CONNECTION_ID&input=1&currency=USD" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "input": "1",
  "currency": "USD"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/formatting/latest/actions/format-currency?${params}`, {
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
| `input` | number | yes | The number to format as currency. |
| `currency` | string | yes | The ISO currency code. Default: `USD`. |
| `locale` | string | no | The locale to use for formatting. Default: `en-US`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "formattedCurrency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `formattedCurrency` | string |  |

## Native endpoint

Through the native Formatting API, this operation is `POST /post` (base URL `https://postman-echo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/format-currency.md) for the provider-specific parameters and requirements.

