# Cloudmersive: Get Country Currency

Retrieves a country's currency from Cloudmersive.

```
GET https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-country-currency
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudmersive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-country-currency?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersive/latest/actions/get-country-currency?${params}`, {
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
| `RawCountryInput` | string | no | Country code or country name to evaluate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "countryFullName": "Ava Chen",
      "currencyEnglishName": "Ava Chen",
      "currencySymbol": "string",
      "isoCurrencyCode": "string",
      "successful": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `countryFullName` | string |  |
| `currencyEnglishName` | string |  |
| `currencySymbol` | string |  |
| `isoCurrencyCode` | string |  |
| `successful` | boolean |  |

## Native endpoint

Through the native Cloudmersive API, this operation is `POST /validate/address/country/get-currency` (base URL `https://api.cloudmersive.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-country-currency.md) for the provider-specific parameters and requirements.

