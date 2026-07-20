# Unleashed: List Suppliers

Retrieves suppliers from your Unleashed supplier directory.

```
GET https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Unleashed `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/unleashed/latest/actions/list-suppliers?${params}`, {
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
      "addresses": [
        {}
      ],
      "currency": {},
      "defaultWarehouse": {},
      "email": "ava@example.com",
      "guid": "string",
      "lastModifiedOn": "string",
      "leadTimeDays": 1,
      "minimumOrderValue": 1,
      "obsolete": true,
      "paymentTerm": "string",
      "phoneNumber": "string",
      "supplierCode": "string",
      "supplierName": "Ava Chen",
      "taxable": true,
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `currency` | object |  |
| `defaultWarehouse` | object |  |
| `email` | string |  |
| `guid` | string |  |
| `lastModifiedOn` | string |  |
| `leadTimeDays` | number |  |
| `minimumOrderValue` | number |  |
| `obsolete` | boolean |  |
| `paymentTerm` | string |  |
| `phoneNumber` | string |  |
| `supplierCode` | string |  |
| `supplierName` | string |  |
| `taxable` | boolean |  |
| `website` | string |  |

## Native endpoint

Through the native Unleashed API, this operation is `GET /Suppliers/:pageNumber` (base URL `https://api.unleashedsoftware.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

