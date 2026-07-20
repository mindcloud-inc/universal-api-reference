# Sumtracker: List Suppliers

Retrieves suppliers from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/list-suppliers?${params}`, {
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
| `code` | string | no | Supplier code. |
| `company_name` | string | no | Supplier company name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "companyName": "Ava Chen",
          "firstName": "Ava",
          "lastName": "Chen",
          "code": "string",
          "email": "ava@example.com",
          "phone": "string",
          "currency": "string",
          "addressLine1": "string",
          "addressLine2": "string",
          "city": "string",
          "state": "string",
          "pincode": "string",
          "country": "string",
          "notes": "string",
          "paymentTerms": "string",
          "id": 1
        }
      ],
      "count": 1,
      "next": "string",
      "previous": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].companyName` | string |  |
| `results[].firstName` | string |  |
| `results[].lastName` | string |  |
| `results[].code` | string |  |
| `results[].email` | string |  |
| `results[].phone` | string |  |
| `results[].currency` | string |  |
| `results[].addressLine1` | string |  |
| `results[].addressLine2` | string |  |
| `results[].city` | string |  |
| `results[].state` | string |  |
| `results[].pincode` | string |  |
| `results[].country` | string |  |
| `results[].notes` | string |  |
| `results[].paymentTerms` | string |  |
| `results[].id` | number |  |
| `count` | number |  |
| `next` | string |  |
| `previous` | object |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/purchases/contacts/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

