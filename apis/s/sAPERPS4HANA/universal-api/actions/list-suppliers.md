# SAP ERP (S/4HANA): List Suppliers

Retrieves suppliers from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-suppliers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-suppliers?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-suppliers?${params}`, {
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
| `top` | number | no | Maximum number of suppliers to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of suppliers to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdByUser": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "deletionIndicator": true,
      "postingIsBlocked": true,
      "purchasingIsBlocked": true,
      "supplier": "string",
      "supplierAccountGroup": "string",
      "supplierFullName": "Ava Chen",
      "supplierName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdByUser` | string | User who created the supplier. |
| `creationDate` | date | Creation date. |
| `deletionIndicator` | boolean | Whether the supplier is marked for deletion. |
| `postingIsBlocked` | boolean | Whether posting is blocked for the supplier. |
| `purchasingIsBlocked` | boolean | Whether purchasing is blocked for the supplier. |
| `supplier` | string | Supplier identifier. |
| `supplierAccountGroup` | string | Supplier account group. |
| `supplierFullName` | string | Full supplier name. |
| `supplierName` | string | Supplier display name. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_Supplier` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-suppliers.md) for the provider-specific parameters and requirements.

