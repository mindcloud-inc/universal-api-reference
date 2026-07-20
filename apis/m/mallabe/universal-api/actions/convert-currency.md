# Mallabe: Convert Currency

Retrieves a currency conversion from Mallabe.

```
GET https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/convert-currency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mallabe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/convert-currency?connectionId=$CONNECTION_ID&to=string&amount=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "to": "string",
  "amount": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mallabe/latest/actions/convert-currency?${params}`, {
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
| `from` | string | no | Source currency code. Default: `EUR`. |
| `to` | string | yes | Target currency code. |
| `amount` | number | yes | Amount to convert. |
| `date` | date | no | Historical conversion date. |
| `webhookUrl` | string | no | Webhook URL for asynchronous callbacks. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "convertedAmount": 1,
      "date": "2026-05-07T12:00:00.000Z",
      "from": "string",
      "fullConvertedAmount": 1,
      "to": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `convertedAmount` | number |  |
| `date` | date |  |
| `from` | string |  |
| `fullConvertedAmount` | number |  |
| `to` | string |  |

## Native endpoint

Through the native Mallabe API, this operation is `POST /currencies/convert` (base URL `https://mallabe.p.rapidapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-currency.md) for the provider-specific parameters and requirements.

