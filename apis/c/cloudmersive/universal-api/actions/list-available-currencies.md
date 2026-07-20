# Cloudmersive: List Available Currencies

Retrieves available currencies and countries from Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/list-available-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/list-available-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/list-available-currencies?${params}`, {
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
      "currencies": [
        {
          "countryIsoTwoLetterCode": "string",
          "countryName": "Ava Chen",
          "countryThreeLetterCode": "string",
          "currencyEnglishName": "Ava Chen",
          "currencySymbol": "string",
          "isEuropeanUnionMember": true,
          "isoCurrencyCode": "string"
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
| `currencies` | array<object> |  |
| `currencies[].countryIsoTwoLetterCode` | string |  |
| `currencies[].countryName` | string |  |
| `currencies[].countryThreeLetterCode` | string |  |
| `currencies[].currencyEnglishName` | string |  |
| `currencies[].currencySymbol` | string |  |
| `currencies[].isEuropeanUnionMember` | boolean |  |
| `currencies[].isoCurrencyCode` | string |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /currency/exchange-rates/list-available` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-currencies.md) for the provider-specific parameters and requirements.

