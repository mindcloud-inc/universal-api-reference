# List Orders with Zoho Backstage

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/portals/:portal_id/events/:event_id/orders`
- **Base URL:** `https://zohoapis.com/backstage`
- **Official documentation:** [List Orders](https://www.zoho.com/backstage/api/v3/get-all-orders.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `portal_id` | path | `string` | yes | The Zoho Backstage portal ID. |
| `event_id` | path | `string` | yes | The Zoho Backstage event ID. |
| `page` | query | `number` | no | Page number for paginated order results. |
| `per_page` | query | `number` | no | Maximum number of orders to return per page. |
| `order_by` | query | `string` | no | Field used to sort orders. |
| `sort_order` | query | `string` | no | Sort direction for the order list. |
| `status` | query | `string` | no | Filter orders by status. |
