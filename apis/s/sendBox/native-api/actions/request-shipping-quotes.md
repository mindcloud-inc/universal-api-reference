# Request Shipping Quotes with SendBox

## Endpoint

- **Method:** `POST`
- **Path:** `/shipping/shipment_delivery_quote`
- **Base URL:** `https://live.sendbox.co`
- **Official documentation:** [Request Shipping Quotes](https://docs.sendbox.co/shipping/request-shipping-quotes)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `channel_code` | body | `string` | yes | Channel the request is being made from; set to api. |
| `currency` | body | `string` | yes | Shop currency. |
| `customs_option` | body | `string` | yes | Customs options. |
| `destination` | body | `object` | yes | Recipient details object. |
| `dimension` | body | `object` | yes | Dimension details object. |
| `incoming_option` | body | `string` | yes | Incoming option; pickup or drop off. |
| `items` | body | `list<object>` | yes | Array of shipment item objects. |
| `origin` | body | `object` | yes | Sender details object. |
| `package_type` | body | `string` | yes | Package type. |
| `pickup_date` | body | `date` | yes | Date package is picked up. |
| `region` | body | `string` | yes | Region the package is shipped from. |
| `service_code` | body | `string` | yes | Can be standard, premium, or expedient. |
| `service_type` | body | `string` | yes | Set to either international or local. |
| `total_value` | body | `number` | yes | Value of shipment. |
| `weight` | body | `number` | yes | Weight of package. |
