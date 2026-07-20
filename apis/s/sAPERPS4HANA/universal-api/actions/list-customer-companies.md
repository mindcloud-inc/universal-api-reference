# SAP ERP (S/4HANA): List Customer Companies

Retrieves customer companies from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-companies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-companies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-companies?${params}`, {
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
| `top` | number | no | Maximum number of customer company records to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of customer company records to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyCode": "string",
      "customer": "string",
      "customerAccountGroup": "string",
      "deletionIndicator": true,
      "paymentTerms": "string",
      "reconciliationAccount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyCode` | string | Company code. |
| `customer` | string | Customer identifier. |
| `customerAccountGroup` | string | Customer account group. |
| `deletionIndicator` | boolean | Whether the customer company assignment is marked for deletion. |
| `paymentTerms` | string | Payment terms. |
| `reconciliationAccount` | string | Reconciliation account for the customer company assignment. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_CustomerCompany` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-companies.md) for the provider-specific parameters and requirements.

