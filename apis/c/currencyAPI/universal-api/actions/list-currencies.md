# CurrencyAPI: List Currencies

Retrieves supported currency definitions from CurrencyAPI.

```
GET https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/list-currencies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CurrencyAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/list-currencies?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/currencyAPI/latest/actions/list-currencies?${params}`, {
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
| `currencies` | string | no | Comma-separated currency codes to return. |
| `type` | string | no | Currency type to return: fiat, metal, or crypto. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "countries": [
        "string"
      ],
      "decimalDigits": 1,
      "iconName": "Ava Chen",
      "name": "Ava Chen",
      "namePlural": "Ava Chen",
      "rounding": 1,
      "symbol": "string",
      "symbolNative": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | ISO currency code |
| `countries` | array<string> | Associated country codes |
| `decimalDigits` | number | Default decimal precision |
| `iconName` | string | Optional icon key |
| `name` | string | Currency display name |
| `namePlural` | string | Plural currency name |
| `rounding` | number | Rounding increment |
| `symbol` | string | Currency symbol |
| `symbolNative` | string | Native currency symbol |
| `type` | string | Currency type |

## Native endpoint

Through the native CurrencyAPI API, this operation is `GET /v3/currencies` (base URL `https://api.currencyapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-currencies.md) for the provider-specific parameters and requirements.

