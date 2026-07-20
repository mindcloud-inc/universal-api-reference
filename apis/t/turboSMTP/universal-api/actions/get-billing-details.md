# turboSMTP: Get Billing Details

Retrieves personal billing details from turboSMTP.

```
GET https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-billing-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a turboSMTP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-billing-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/turboSMTP/latest/actions/get-billing-details?${params}`, {
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
      "address_1": "string",
      "address_2": "string",
      "billing_contact": "string",
      "city": "string",
      "company_name": "Ava Chen",
      "country": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "last_name": "Chen",
      "offers_acceptance": true,
      "phone_number": "string",
      "state": "string",
      "vat": 1,
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_1` | string |  |
| `address_2` | string |  |
| `billing_contact` | string |  |
| `city` | string |  |
| `company_name` | string |  |
| `country` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `last_name` | string |  |
| `offers_acceptance` | boolean |  |
| `phone_number` | string |  |
| `state` | string |  |
| `vat` | number |  |
| `zip_code` | string |  |

## Native endpoint

Through the native turboSMTP API, this operation is `GET /billing/details` (base URL `https://pro.api.serversmtp.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-billing-details.md) for the provider-specific parameters and requirements.

