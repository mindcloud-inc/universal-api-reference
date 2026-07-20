# Shipcloud: Get Invoice Address

Retrieves the invoice address from Shipcloud.

```
GET https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-invoice-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shipcloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-invoice-address?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipcloud/latest/actions/get-invoice-address?${params}`, {
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
      "care_of": "string",
      "city": "string",
      "company": "string",
      "country": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "phone": "string",
      "state": "string",
      "street": "string",
      "street_no": "string",
      "zip_code": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `care_of` | string |  |
| `city` | string |  |
| `company` | string |  |
| `country` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `phone` | string |  |
| `state` | string |  |
| `street` | string |  |
| `street_no` | string |  |
| `zip_code` | string |  |

## Native endpoint

Through the native Shipcloud API, this operation is `GET /invoice_address` (base URL `https://api.shipcloud.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-invoice-address.md) for the provider-specific parameters and requirements.

