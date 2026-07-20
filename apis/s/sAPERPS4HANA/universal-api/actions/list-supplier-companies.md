# SAP ERP (S/4HANA): List Supplier Companies

Retrieves supplier companies from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-supplier-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-supplier-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-supplier-companies?${params}`, {
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
| `top` | number | no | Maximum number of supplier company records to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of supplier company records to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyCode": "string",
      "companyCodeName": "Ava Chen",
      "currency": "string",
      "deletionIndicator": true,
      "paymentTerms": "string",
      "reconciliationAccount": "string",
      "supplier": "string",
      "supplierAccountGroup": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyCode` | string | Company code. |
| `companyCodeName` | string | Company code name. |
| `currency` | string | Currency code. |
| `deletionIndicator` | boolean | Whether the supplier company assignment is marked for deletion. |
| `paymentTerms` | string | Payment terms. |
| `reconciliationAccount` | string | Reconciliation account for the supplier company assignment. |
| `supplier` | string | Supplier identifier. |
| `supplierAccountGroup` | string | Supplier account group. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_SupplierCompany` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-supplier-companies.md) for the provider-specific parameters and requirements.

