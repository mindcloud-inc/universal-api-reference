# Calculate Landed Cost with SendBox

## Endpoint

- **Method:** `POST`
- **Path:** `/shipping/landed_cost_estimate`
- **Base URL:** `https://live.sendbox.co`
- **Official documentation:** [Calculate Landed Cost](https://docs.sendbox.co/shipping/calculate-landed-cost)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | body | `string` | no | Webhook URL for tracking updates. |
| `channel_code` | body | `string` | yes | Channel the request is being made from; set to api. |
| `customs_option` | body | `string` | yes | Customs options. |
| `destination` | body | `object` | yes | Recipient details object. |
| `dimension` | body | `object` | yes | Dimension details object. |
| `incoming_option` | body | `string` | yes | Incoming option; pickup or drop off. |
| `items` | body | `list<object>` | yes | Array of shipment item objects. |
| `origin` | body | `object` | yes | Sender details object. |
| `package_type` | body | `string` | yes | Package type. |
| `pickup_date` | body | `date` | yes | Date package is picked up. |
| `region` | body | `string` | yes | Region the shipment is being shipped from. |
| `service_code` | body | `string` | yes | Can be international, nation-wide, or local. |
| `service_type` | body | `string` | yes | Service type. |
| `total_value` | body | `number` | yes | Value of shipment. |
| `weight` | body | `number` | yes | Weight of package. |
