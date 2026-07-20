# Add Order with Cloudprinter.com

Creates an order in Cloudprinter.com.

## Endpoint

- **Method:** `POST`
- **Path:** `/cloudcore/1.0/orders/add`
- **Base URL:** `https://api.cloudprinter.com`
- **Official documentation:** [Add Order](https://docs.cloudprinter.com/client/cloudprinter-core-api-v1-0#add-order)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reference` | body | `string` | yes | Client order reference. |
| `email` | body | `string` | yes | Customer email address for the order. |
| `addresses[]` | body | `array<object>` | yes | One or more delivery addresses. |
| `addresses[].type` | body | `string` | yes | Address type. Cloudprinter expects delivery for order creation. |
| `addresses[].firstname` | body | `string` | yes | Recipient first name. |
| `addresses[].lastname` | body | `string` | yes | Recipient last name. |
| `addresses[].street1` | body | `string` | yes | Primary street line for the delivery address. |
| `addresses[].zip` | body | `string` | yes | Postal or ZIP code for the delivery address. |
| `addresses[].city` | body | `string` | yes | City for the delivery address. |
| `addresses[].country` | body | `string` | yes | Delivery country in ISO 3166-1 alpha-2 format. |
| `addresses[].email` | body | `string` | yes | Email for the delivery address contact. |
| `addresses[].phone` | body | `string` | yes | Phone number for the delivery address contact. Required by the live API. |
| `items[]` | body | `array<object>` | yes | One or more order items. |
| `items[].reference` | body | `string` | yes | Client item reference. Must match the reference used when quoting. |
| `items[].product` | body | `string` | yes | Cloudprinter product reference. |
| `items[].count` | body | `string` | yes | Number of copies to produce for this item. |
| `items[].quote` | body | `string` | no | Quote hash returned by Get Order Quote for this item. |
| `shipping_level` | body | `string` | no | Preferred shipping level when no quote hash is supplied. |
| `items[].title` | body | `string` | no | Optional customer-facing item title. |
| `items[].options[]` | body | `array<object>` | no | Optional item options. Cloudprinter expects an array value even when empty. |
| `items[].files[]` | body | `array<object>` | yes | Files to print for this item. |
| `items[].files[].type` | body | `string` | yes | File type expected by the selected product. |
| `items[].files[].url` | body | `string` | yes | HTTPS URL where Cloudprinter can download the print file. |
| `items[].files[].md5sum` | body | `string` | yes | MD5 checksum used by Cloudprinter to validate the downloaded file. |
