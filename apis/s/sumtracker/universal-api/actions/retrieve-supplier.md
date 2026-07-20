# Sumtracker: Retrieve Supplier

Retrieves a supplier from Sumtracker.

```
GET https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/retrieve-supplier
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumtracker `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/retrieve-supplier?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumtracker/latest/actions/retrieve-supplier?${params}`, {
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
| `id` | string | yes | Supplier ID. |

## Response

```json
{
  "success": true,
  "data": [
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyName` | string |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `code` | string |  |
| `email` | string |  |
| `phone` | string |  |
| `currency` | string |  |
| `addressLine1` | string |  |
| `addressLine2` | string |  |
| `city` | string |  |
| `state` | string |  |
| `pincode` | string |  |
| `country` | string |  |
| `notes` | string |  |
| `paymentTerms` | string |  |
| `id` | number |  |

## Native endpoint

Through the native Sumtracker API, this operation is `GET /api/version/2025-03/purchases/contacts/:id/` (base URL `https://inventory-api.sumtracker.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-supplier.md) for the provider-specific parameters and requirements.

