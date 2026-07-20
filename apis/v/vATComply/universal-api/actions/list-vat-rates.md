# VAT Comply: List VAT Rates

Retrieves VAT rates from VAT Comply.

```
GET https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/list-vat-rates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VAT Comply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/list-vat-rates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vATComply/latest/actions/list-vat-rates?${params}`, {
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
| `countryCode` | string | no | Filter by EU member state code, for example DE or FR. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country_code": "string",
      "country_name": "Ava Chen",
      "currency": "string",
      "member_state": true,
      "parking_rate": 1,
      "rate_categories": {},
      "rate_comments": {},
      "reduced_rates": [
        1
      ],
      "standard_rate": 1,
      "super_reduced_rate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country_code` | string |  |
| `country_name` | string |  |
| `currency` | string |  |
| `member_state` | boolean |  |
| `parking_rate` | number |  |
| `rate_categories` | object |  |
| `rate_comments` | object |  |
| `reduced_rates` | array<number> |  |
| `standard_rate` | number |  |
| `super_reduced_rate` | number |  |

## Native endpoint

Through the native VAT Comply API, this operation is `GET /vat_rates` (base URL `https://api.vatcomply.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vat-rates.md) for the provider-specific parameters and requirements.

