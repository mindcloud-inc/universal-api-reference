# Create Customer with GoCanvas

## Endpoint

- **Method:** `POST`
- **Path:** `/customers`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Create Customer](https://api.gocanvas.com/api/v3/docs#create-a-customer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customer_type` | body | `list` | yes | An individual or a business customer. Accepted values: `business`, `individual`. |
| `business_name` | body | `string` | no | Required when customer type is business. |
| `contact_role` | body | `string` | no | Role of the customer's contact person. |
| `contact_first_name` | body | `string` | no | Required when customer type is individual. |
| `contact_last_name` | body | `string` | no | Required when customer type is individual. |
| `contact_email` | body | `string` | no | Email address of the customer's contact person. |
| `contact_phone` | body | `string` | no | Phone number of the customer's contact person. |
| `contact_preference` | body | `string` | no | Preferred method of contact. |
| `notes` | body | `string` | no | Longer description of the customer. |
| `code` | body | `string` | no | Alphanumeric code uniquely identifying the customer. |
