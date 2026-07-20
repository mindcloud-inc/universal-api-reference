# SAP ERP (S/4HANA): List Customer Sales Areas

Retrieves customer sales areas from SAP ERP (S/4HANA).

```
GET https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-sales-areas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SAP ERP (S/4HANA) `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-sales-areas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sAPERPS4HANA/latest/actions/list-customer-sales-areas?${params}`, {
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
| `top` | number | no | Maximum number of customer sales areas to return. Default: `10`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `skip` | number | no | Number of customer sales areas to skip before returning results. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "customer": "string",
      "customerGroup": "string",
      "customerPaymentTerms": "string",
      "deletionIndicator": true,
      "distributionChannel": "string",
      "division": "string",
      "salesOrganization": "string",
      "shippingCondition": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string | Currency code. |
| `customer` | string | Customer identifier. |
| `customerGroup` | string | Customer group. |
| `customerPaymentTerms` | string | Customer payment terms. |
| `deletionIndicator` | boolean | Whether the customer sales area is marked for deletion. |
| `distributionChannel` | string | Distribution channel. |
| `division` | string | Division. |
| `salesOrganization` | string | Sales organization. |
| `shippingCondition` | string | Shipping condition. |

## Native endpoint

Through the native SAP ERP (S/4HANA) API, this operation is `GET /A_CustomerSalesArea` (base URL `https://sandbox.api.sap.com/s4hanacloud/sap/opu/odata/sap/API_BUSINESS_PARTNER`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-customer-sales-areas.md) for the provider-specific parameters and requirements.

