# Zoho Inventory: Create Package

Creates a new package in Zoho Inventory.

```
POST https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/create-package
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/create-package" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "{{credentials.organizationId}}",
  "salesOrderId": "string",
  "date": "string",
  "lineItems[]": [
    {}
  ],
  "lineItems[].soLineItemId": "string",
  "lineItems[].quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/create-package', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "{{credentials.organizationId}}",
    "salesOrderId": "string",
    "date": "string",
    "lineItems[]": [{}],
    "lineItems[].soLineItemId": "string",
    "lineItems[].quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Zoho Inventory organization ID to run this request against. Default: `{{credentials.organizationId}}`. |
| `salesOrderId` | string | yes |  |
| `packageNumber` | string | no |  |
| `date` | string | yes |  |
| `notes` | string | no |  |
| `lineItems[]` | array<object> | yes |  |
| `lineItems[].soLineItemId` | string | yes |  |
| `lineItems[].quantity` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_time": "string",
      "customer_id": "string",
      "customer_name": "Ava Chen",
      "date": "string",
      "last_modified_time": "string",
      "line_items": [
        {}
      ],
      "notes": "string",
      "package_id": "string",
      "package_number": "string",
      "salesorder_id": "string",
      "salesorder_number": "string",
      "shipment_order": {},
      "status": "string",
      "tracking_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_time` | string |  |
| `customer_id` | string |  |
| `customer_name` | string |  |
| `date` | string |  |
| `last_modified_time` | string |  |
| `line_items` | array<object> |  |
| `notes` | string |  |
| `package_id` | string |  |
| `package_number` | string |  |
| `salesorder_id` | string |  |
| `salesorder_number` | string |  |
| `shipment_order` | object |  |
| `status` | string |  |
| `tracking_number` | string |  |

## Native endpoint

Through the native Zoho Inventory API, this operation is `POST /packages` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-package.md) for the provider-specific parameters and requirements.

