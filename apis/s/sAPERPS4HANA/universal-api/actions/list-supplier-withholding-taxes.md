# SAP ERP (S/4HANA): List Supplier Withholding Taxes

Retrieves supplier withholding taxes from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-supplier-withholding-taxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-supplier-withholding-taxes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-supplier-withholding-taxes?${params}`, {
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
| `top` | number | no | Maximum number of supplier withholding tax records to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of supplier withholding tax records to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "companyCode": "string",
      "isWithholdingTaxSubject": true,
      "supplier": "string",
      "withholdingTaxCode": "string",
      "withholdingTaxExmptPercent": 1,
      "withholdingTaxNumber": "string",
      "withholdingTaxType": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyCode` | string | Company code. |
| `isWithholdingTaxSubject` | boolean | Whether the supplier is subject to withholding tax. |
| `supplier` | string | Supplier identifier. |
| `withholdingTaxCode` | string | Withholding tax code. |
| `withholdingTaxExmptPercent` | number | Withholding tax exemption percentage. |
| `withholdingTaxNumber` | string | Withholding tax number. |
| `withholdingTaxType` | string | Withholding tax type. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_SupplierWithHoldingTax` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-supplier-withholding-taxes.md) for the provider-specific parameters and requirements.

