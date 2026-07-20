# Ascora: List Suppliers

Retrieves suppliers from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-suppliers?${params}`, {
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
| `businessNumber` | string | no | Performs an exact match against the Business Number of the Supplier, ignoring white space. |
| `supplierName` | string | no | Performs a partial match against the Supplier Name. |
| `supplierNumber` | string | no | Performs a partial match against the Supplier Number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "businessNumber": "string",
          "contactFirstName": "Ava",
          "contactLastName": "Chen",
          "emailAddress": "ava@example.com",
          "expenseAccount": "string",
          "fax": "string",
          "invoiceDueDaysType": 1,
          "mobile": "string",
          "name": "Ava Chen",
          "notes": "string",
          "phone": "string",
          "postalLine1": "string",
          "postalLine2": "string",
          "postalPostcode": "string",
          "postalState": "string",
          "postalSuburb": "string",
          "streetLine1": "string",
          "streetLine2": "string",
          "streetPostcode": "string",
          "streetState": "string",
          "streetSuburb": "string",
          "supplierId": "string",
          "supplierNumber": "string"
        }
      ],
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].businessNumber` | string |  |
| `results[].contactFirstName` | string |  |
| `results[].contactLastName` | string |  |
| `results[].emailAddress` | string |  |
| `results[].expenseAccount` | string |  |
| `results[].fax` | string |  |
| `results[].invoiceDueDaysType` | number |  |
| `results[].mobile` | string |  |
| `results[].name` | string |  |
| `results[].notes` | string |  |
| `results[].phone` | string |  |
| `results[].postalLine1` | string |  |
| `results[].postalLine2` | string |  |
| `results[].postalPostcode` | string |  |
| `results[].postalState` | string |  |
| `results[].postalSuburb` | string |  |
| `results[].streetLine1` | string |  |
| `results[].streetLine2` | string |  |
| `results[].streetPostcode` | string |  |
| `results[].streetState` | string |  |
| `results[].streetSuburb` | string |  |
| `results[].supplierId` | string |  |
| `results[].supplierNumber` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Ascora API, this operation is `GET /Suppliers/Suppliers` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

