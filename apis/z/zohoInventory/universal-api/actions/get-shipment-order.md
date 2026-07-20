# Zoho Inventory: Get Shipment Order

Retrieves a shipment order from Zoho Inventory.

```
GET https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/get-shipment-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/get-shipment-order?connectionId=$CONNECTION_ID&shipmentOrderId=string&organizationId=%7B%7Bcredentials.organizationId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "shipmentOrderId": "string",
  "organizationId": "{{credentials.organizationId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/get-shipment-order?${params}`, {
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
| `shipmentOrderId` | string | yes | The Zoho Inventory shipmentorder_id for the shipment order. |
| `organizationId` | string | yes | Zoho Inventory organization ID to run this request against. Default: `{{credentials.organizationId}}`. |

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
      "delivery_method": "string",
      "last_modified_time": "string",
      "line_items": [
        {}
      ],
      "notes": "string",
      "packages": [
        {}
      ],
      "salesorder_id": "string",
      "salesorder_number": "string",
      "shipment_id": "string",
      "shipment_number": "string",
      "status": "string",
      "total": 1,
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
| `delivery_method` | string |  |
| `last_modified_time` | string |  |
| `line_items` | array<object> |  |
| `notes` | string |  |
| `packages` | array<object> |  |
| `salesorder_id` | string |  |
| `salesorder_number` | string |  |
| `shipment_id` | string |  |
| `shipment_number` | string |  |
| `status` | string |  |
| `total` | number |  |
| `tracking_number` | string |  |

## Native endpoint

Through the native Zoho Inventory API, this operation is `GET /shipmentorders/:shipmentorder_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-shipment-order.md) for the provider-specific parameters and requirements.

