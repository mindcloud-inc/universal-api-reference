# Create Shipment with SendBox

## Endpoint

- **Method:** `POST`
- **Path:** `/shipping/shipments`
- **Base URL:** `https://live.sendbox.co`
- **Official documentation:** [Create Shipment](https://docs.sendbox.co/shipping/create-new-shipment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `callback_url` | body | `string` | no | Webhook URL to receive tracking updates. |
| `channel_code` | body | `string` | yes | Channel the request is being made from; set to api. |
| `destination` | body | `object` | yes | Recipient details object. |
| `incoming_option` | body | `string` | yes | Incoming option; pickup or dropoff. |
| `items` | body | `list<object>` | yes | Array of shipment item objects. |
| `origin` | body | `object` | yes | Sender details object. |
| `package_type` | body | `string` | yes | Package type. |
| `pickup_date` | body | `date` | yes | Date package is picked up. |
| `region` | body | `string` | yes | Region the shipment is being shipped from. |
| `service_code` | body | `string` | yes | Can be international, nation-wide, or local. |
| `total_value` | body | `number` | yes | Value of shipment. |
| `weight` | body | `number` | yes | Weight of package. |
