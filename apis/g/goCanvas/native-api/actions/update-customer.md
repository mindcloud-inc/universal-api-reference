# Update Customer with GoCanvas

## Endpoint

- **Method:** `PATCH`
- **Path:** `/customers/:customerId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Update Customer](https://api.gocanvas.com/api/v3/docs#update-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customerId` | path | `number` | yes | Identifier of the customer to update. |
| `customer_type` | body | `list` | no | Customer type. The documentation conflicts on whether it is required for PATCH. Accepted values: `business`, `individual`. |
| `business_name` | body | `string` | no | Business name; documented as required for business customers. |
| `contact_role` | body | `string` | no | Role of the customer's contact person. |
| `contact_first_name` | body | `string` | no | Contact first name; documented as required for individual customers. |
| `contact_last_name` | body | `string` | no | Contact last name; documented as required for individual customers. |
| `contact_email` | body | `string` | no | Email of the contact person. |
| `contact_phone` | body | `string` | no | Phone of the contact person. |
| `contact_preference` | body | `string` | no | Preferred contact method. |
| `notes` | body | `string` | no | Longer description of the customer. |
| `default_site_id` | body | `number` | no | Primary site ID when multiple site IDs are provided. |
| `code` | body | `string` | no | Alphanumeric customer identifier. |
| `site_ids[]` | body | `array<number>` | no | Site IDs to add. The first is primary unless Default Site ID is provided. |
