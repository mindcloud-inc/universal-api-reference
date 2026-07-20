# SAP ERP (S/4HANA): List Supplier Partner Functions

Retrieves supplier partner functions from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-supplier-partner-functions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-supplier-partner-functions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-supplier-partner-functions?${params}`, {
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
| `top` | number | no | Maximum number of supplier partner functions to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of supplier partner functions to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdByUser": "string",
      "creationDate": "2026-05-07T12:00:00.000Z",
      "defaultPartner": true,
      "partnerCounter": "string",
      "partnerFunction": "string",
      "purchasingOrganization": "string",
      "referenceSupplier": "string",
      "supplier": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdByUser` | string | User who created the supplier partner function. |
| `creationDate` | date | Creation date. |
| `defaultPartner` | boolean | Whether this is the default partner. |
| `partnerCounter` | string | Partner counter. |
| `partnerFunction` | string | Partner function. |
| `purchasingOrganization` | string | Purchasing organization. |
| `referenceSupplier` | string | Reference supplier. |
| `supplier` | string | Supplier identifier. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_SupplierPartnerFunc` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-supplier-partner-functions.md) for the provider-specific parameters and requirements.

