# SAP ERP (S/4HANA): List Customers

Retrieves customers from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customers?${params}`, {
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
| `top` | number | no | Maximum number of customers to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of customers to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdByUser": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "customer": "string",
      "customerAccountGroup": "string",
      "customerFullName": "Ava Chen",
      "customerName": "Ava Chen",
      "deletionIndicator": true,
      "postingIsBlocked": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdByUser` | string | User who created the customer. |
| `creationDate` | date | Creation date. |
| `customer` | string | Customer identifier. |
| `customerAccountGroup` | string | Customer account group. |
| `customerFullName` | string | Full customer name. |
| `customerName` | string | Customer display name. |
| `deletionIndicator` | boolean | Whether the customer is marked for deletion. |
| `postingIsBlocked` | boolean | Whether posting is blocked for the customer. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_Customer` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customers.md) for the provider-specific parameters and requirements.

