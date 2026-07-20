# Kiwili: Get Currency Details

Retrieves details for a currency in Kiwili.

```
GET https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-currency-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwili `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-currency-details?connectionId=$CONNECTION_ID&currency_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "currency_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwili/latest/actions/get-currency-details?${params}`, {
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
| `currency_id` | string | yes | The Kiwili currency ID. Use the string 0 for the default record when needed. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CountryCode": "string",
      "CountryName": "Ava Chen",
      "CurrencyCode": "string",
      "CurrencyName": "Ava Chen",
      "CurrencySymbol": "string",
      "CurrencySymbolHex": "string",
      "Id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CountryCode` | string |  |
| `CountryName` | string |  |
| `CurrencyCode` | string |  |
| `CurrencyName` | string |  |
| `CurrencySymbol` | string |  |
| `CurrencySymbolHex` | string |  |
| `Id` | number |  |

## Native endpoint

Through the native Kiwili API, this operation is `GET /currency/:currency_id` (base URL `https://mindcloud.kiwili.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-currency-details.md) for the provider-specific parameters and requirements.

