# Housecall Pro: Bulk Update Estimate Option Line Items



```
PUT https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/bulk-update-estimate-option-line-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/bulk-update-estimate-option-line-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "estimateId": "csr_48c56f1d6e304fd3bd64069968d58d3b",
  "optionId": "est_4c3bbad072de4216a21da7918c8e5854",
  "lineItems[].name": "Diagnostic Add-on"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/bulk-update-estimate-option-line-items', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "estimateId": "csr_48c56f1d6e304fd3bd64069968d58d3b",
    "optionId": "est_4c3bbad072de4216a21da7918c8e5854",
    "lineItems[].name": "Diagnostic Add-on"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `estimateId` | string | yes | The estimate to update. Example: `csr_48c56f1d6e304fd3bd64069968d58d3b`. |
| `optionId` | string | yes | The estimate option to update. Example: `est_4c3bbad072de4216a21da7918c8e5854`. |
| `lineItems[]` | array<object> | no | Line items to update or create. Example: `[object Object]`. |
| `lineItems[].name` | string | yes | Line item name. Example: `Diagnostic Add-on`. |
| `lineItems[].unitPrice` | number | no | Line item unit price. Example: `99`. |
| `lineItems[].quantity` | number | no | Line item quantity. Example: `1`. |
| `lineItems[].description` | string | no | Line item description. Example: `Added during stage 3 buildout.`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `lineItems[].id` | string | no | Existing line item id to update. Example: `lin_123`. |
| `lineItems[].serviceItemId` | string | no | Service item id for the line item. Example: `srv_123`. |
| `lineItems[].serviceItemType` | list<string> | no | Service item type for the line item. One of: `market_place`, `organizational`, `pricebook_material`. |
| `lineItems[].unitCost` | number | no | Line item unit cost. Example: `50`. |
| `lineItems[].kind` | list<string> | no | Line item kind. One of: `fixed discount`, `fixed gratuity`, `labor`, `materials`, `percent discount`. Default: `labor`. |
| `lineItems[].taxable` | boolean | no | Whether the line item is taxable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Updated estimate option line items. |
| `object` | string | Response object type. |
| `url` | string | Provider relative URL for the line item collection. |

## Native endpoint

Through the native Housecall Pro API, this operation is `PUT /estimates/:estimate_id/options/:option_id/line_items/bulk_update` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-update-estimate-option-line-items.md) for the provider-specific parameters and requirements.

