# BigCommerce (B2B): Get Company Credit



```
GET https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-company-credit
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BigCommerce (B2B) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-company-credit?connectionId=$CONNECTION_ID&companyId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bigCommerceB2B/latest/actions/get-company-credit?${params}`, {
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
| `companyId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "availableCredit": {},
        "creditCurrency": "string",
        "creditEnabled": true,
        "creditHold": true,
        "limitPurchases": true
      },
      "meta": {
        "message": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data.availableCredit` | object |  |
| `data.creditCurrency` | string |  |
| `data.creditEnabled` | boolean |  |
| `data.creditHold` | boolean |  |
| `data.limitPurchases` | boolean |  |
| `meta.message` | string |  |

## Native endpoint

Through the native BigCommerce (B2B) API, this operation is `GET companies/:companyId/credit` (base URL `https://api-b2b.bigcommerce.com/api/v3/io/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-credit.md) for the provider-specific parameters and requirements.

