# Cloudmersive Currency: Convert Currency

Converts a currency amount in Cloudmersive Currency.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/convert-currency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Currency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/convert-currency?connectionId=$CONNECTION_ID&source=string&destination=string&price=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "source": "string",
  "destination": "string",
  "price": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/convert-currency?${params}`, {
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
| `source` | string | yes | Source currency three-digit ISO 4217 code, such as USD or EUR. |
| `destination` | string | yes | Destination currency three-digit ISO 4217 code, such as USD or EUR. |
| `price` | number | yes | Input price in the source currency, such as 19.99. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ConvertedPrice": 1,
      "CurrencySymbol": "string",
      "FormattedPriceAsString": "string",
      "ISOCurrencyCode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ConvertedPrice` | number | Converted price in the destination currency. |
| `CurrencySymbol` | string | Destination currency symbol. |
| `FormattedPriceAsString` | string | Formatted destination price string. |
| `ISOCurrencyCode` | string | ISO 4217 destination currency code. |

## Native endpoint

Through the native Cloudmersive Currency API, this operation is `POST /currency/exchange-rates/convert/:source/to/:destination` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-currency.md) for the provider-specific parameters and requirements.

