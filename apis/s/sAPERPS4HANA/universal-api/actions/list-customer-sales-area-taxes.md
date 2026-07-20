# SAP ERP (S/4HANA): List Customer Sales Area Taxes

Retrieves customer sales area taxes from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-sales-area-taxes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-sales-area-taxes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-sales-area-taxes?${params}`, {
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
| `top` | number | no | Maximum number of customer sales area tax records to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of customer sales area tax records to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customer": "string",
      "customerTaxCategory": "string",
      "customerTaxClassification": "string",
      "departureCountry": "string",
      "distributionChannel": "string",
      "division": "string",
      "salesOrganization": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customer` | string | Customer identifier. |
| `customerTaxCategory` | string | Customer tax category. |
| `customerTaxClassification` | string | Customer tax classification. |
| `departureCountry` | string | Departure country. |
| `distributionChannel` | string | Distribution channel. |
| `division` | string | Division. |
| `salesOrganization` | string | Sales organization. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_CustomerSalesAreaTax` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-sales-area-taxes.md) for the provider-specific parameters and requirements.

