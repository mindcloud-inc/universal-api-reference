# Asset Infinity: List Vendors and Customers

Retrieves vendors and customers from Asset Infinity.

```
GET https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/list-vendors-and-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asset Infinity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/list-vendors-and-customers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/assetInfinity/latest/actions/list-vendors-and-customers?${params}`, {
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
      "data": [
        {
          "city": "string",
          "contactPerson": "string",
          "contactPhone1": "string",
          "createdBy": "string",
          "createdDate": "2026-05-07T12:00:00.000Z",
          "cstNo": "string",
          "email1": "ava@example.com",
          "isCustomer": true,
          "isTicketAssignee": true,
          "isTicketReportedBy": true,
          "panNo": "string",
          "postalCode": "string",
          "remarksNotes": "string",
          "rowIndexNumber": 1,
          "serviceTaxNo": "string",
          "state": "string",
          "vatNo": "string",
          "vendorAddress1": "string",
          "vendorAddress2": "string",
          "vendorId": 1,
          "vendorName": "Ava Chen",
          "vendorNumber": "string"
        }
      ],
      "isSuccess": true,
      "message": "string",
      "statusCode": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].city` | string |  |
| `data[].contactPerson` | string |  |
| `data[].contactPhone1` | string |  |
| `data[].createdBy` | string |  |
| `data[].createdDate` | date |  |
| `data[].cstNo` | string |  |
| `data[].email1` | string |  |
| `data[].isCustomer` | boolean |  |
| `data[].isTicketAssignee` | boolean |  |
| `data[].isTicketReportedBy` | boolean |  |
| `data[].panNo` | string |  |
| `data[].postalCode` | string |  |
| `data[].remarksNotes` | string |  |
| `data[].rowIndexNumber` | number |  |
| `data[].serviceTaxNo` | string |  |
| `data[].state` | string |  |
| `data[].vatNo` | string |  |
| `data[].vendorAddress1` | string |  |
| `data[].vendorAddress2` | string |  |
| `data[].vendorId` | number |  |
| `data[].vendorName` | string |  |
| `data[].vendorNumber` | string |  |
| `isSuccess` | boolean |  |
| `message` | string |  |
| `statusCode` | number |  |

## Native endpoint

Through the native Asset Infinity API, this operation is `POST VendorCustomerList` (base URL `https://api.assetinfinity.io/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-vendors-and-customers.md) for the provider-specific parameters and requirements.

