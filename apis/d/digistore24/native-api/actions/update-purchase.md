# Update Purchase with Digistore24

Updates an existing purchase in Digistore24.

## Endpoint

- **Method:** `PUT`
- **Path:** `/updatePurchase`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Update Purchase](https://digistore24.com/api/docs/paths/updatePurchase.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `purchase_id` | query | `string` | yes | Purchase ID |
| `tracking_param` | body | `string` | no | Vendor tracking key |
| `custom` | body | `string` | no | Custom field |
| `unlock_invoices` | body | `boolean` | no | Restore buyer invoice access |
| `next_payment_at` | body | `string` | no | Next payment date/time |
