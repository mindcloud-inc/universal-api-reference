# SalesDrive: List Currency Rates

Retrieves current currency rates from SalesDrive.

```
GET https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-currency-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SalesDrive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-currency-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/salesDrive/latest/actions/list-currency-rates?${params}`, {
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
      "abbreviation": "string",
      "code": "string",
      "rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abbreviation` | string | Currency symbol or abbreviation. |
| `code` | string | Currency code. |
| `rate` | number | Currency rate. |

## Native endpoint

Through the native SalesDrive API, this operation is `GET /api/currencies/` (base URL `https://{{credentials.account}}.salesdrive.me`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-currency-rates.md) for the provider-specific parameters and requirements.

