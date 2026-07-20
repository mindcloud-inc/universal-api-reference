# Cerbo: Create Inventory

Creates a new inventory item in Cerbo.

```
POST https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cerbo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-inventory" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "linked_product_type": "https://example.com",
  "charge_id": 1,
  "preferred_stock_level": 1,
  "current_quantity": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cerbo/latest/actions/create-inventory', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "linked_product_type": "https://example.com",
    "charge_id": 1,
    "preferred_stock_level": 1,
    "current_quantity": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the inventory item |
| `linked_product_type` | string | yes | Type of linked product: - `rxs`: Links to a medication in the drugs database - `plan_other`: Links to a supplement - `general`: General inventory item (no linked product) |
| `charge_id` | number | yes | ID of the associated charge in the charge master |
| `preferred_stock_level` | number | yes | Target stock level to maintain |
| `current_quantity` | number | yes | Current quantity in stock |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nickname` | string | no | Short nickname for the item |
| `linked_product_id` | number | no | ID of the linked product. Required for "rxs" and "plan_other" types. |
| `preferred_restock_level` | number | no | Level at which to trigger restocking |
| `manufacturer` | string | no | Manufacturer name |
| `expiration_date` | date | no | Expiration date (must be in the future) |
| `lot_number` | string | no | Lot number for tracking |
| `discontinued` | boolean | no | Whether the item is discontinued |
| `date_discontinued` | date | no | Date the item was discontinued |
| `external_identifier` | string | no | External system identifier for integration |
| `location` | string | no | Location name (for multi-location practices) |
| `package_properties.ndc_code` | string | no | National Drug Code (for medications) |
| `package_properties.generic_for` | string | no | Brand name this is generic for |
| `package_properties.charge_per_dose` | string | no | Charge amount per dose |
| `package_properties.charge_per_dispense` | string | no | Charge amount per dispense |
| `package_properties.cost_per_dose` | string | no | Cost per dose |
| `package_properties.patient_information_url` | string | no | URL to patient information sheet |
| `package_properties.package_form` | string | no | Form of packaging |
| `package_properties.product_code` | string | no | Product code |
| `package_properties.description` | string | no | Product description/notes |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charge_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "current_quantity": 1,
      "id": 1,
      "linked_product_id": 1,
      "linked_product_type": "https://example.com",
      "name": "Ava Chen",
      "preferred_stock_level": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charge_id` | number |  |
| `created` | date |  |
| `current_quantity` | number |  |
| `id` | number |  |
| `linked_product_id` | number |  |
| `linked_product_type` | string |  |
| `name` | string |  |
| `preferred_stock_level` | number |  |

## Native endpoint

Through the native Cerbo API, this operation is `POST /inventory` (base URL `https://{{credentials.tenant}}.md-hq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-inventory.md) for the provider-specific parameters and requirements.

