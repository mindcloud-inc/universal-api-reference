# Cloudmersive Currency: List Available Currencies

Retrieves available currencies from Cloudmersive Currency.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/list-available-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive Currency `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/list-available-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveCurrency/latest/actions/list-available-currencies?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "Currencies": [
        {
          "CountryISOTwoLetterCode": "string",
          "CountryName": "Ava Chen",
          "CountryThreeLetterCode": "string",
          "CurrencyEnglishName": "Ava Chen",
          "CurrencySymbol": "string",
          "IsEuropeanUnionMember": true,
          "ISOCurrencyCode": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Currencies` | array<object> | Available currencies and corresponding countries. |
| `Currencies[].CountryISOTwoLetterCode` | string | Two-letter ISO 3166-1 country code. |
| `Currencies[].CountryName` | string | Country name. |
| `Currencies[].CountryThreeLetterCode` | string | Three-letter ISO 3166-1 country code. |
| `Currencies[].CurrencyEnglishName` | string | English currency name. |
| `Currencies[].CurrencySymbol` | string | Currency symbol. |
| `Currencies[].IsEuropeanUnionMember` | boolean | Whether the country is currently an EU member. |
| `Currencies[].ISOCurrencyCode` | string | ISO 4217 currency three-letter code. |

## Native endpoint

Through the native Cloudmersive Currency API, this operation is `POST /currency/exchange-rates/list-available` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-currencies.md) for the provider-specific parameters and requirements.

