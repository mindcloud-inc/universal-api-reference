# Create Address with Commerce Layer

## Endpoint

- **Method:** `POST`
- **Path:** `/api/addresses`
- **Base URL:** `{coreApiEndpoint}`
- **Official documentation:** [Create Address](https://docs.commercelayer.io/core-api-reference/addresses/create)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.business` | body | `boolean` | no | Whether the address belongs to a business. |
| `data.attributes.first_name` | body | `string` | yes | The first name for the address contact. |
| `data.attributes.last_name` | body | `string` | yes | The last name for the address contact. |
| `data.attributes.company` | body | `string` | no | The company name for a business address. |
| `data.attributes.line_1` | body | `string` | yes | The first address line. |
| `data.attributes.line_2` | body | `string` | no | The second address line. |
| `data.attributes.city` | body | `string` | yes | The city for the address. |
| `data.attributes.zip_code` | body | `string` | yes | The postal code for the address. |
| `data.attributes.state_code` | body | `string` | no | The state or province code for the address. |
| `data.attributes.country_code` | body | `string` | yes | The ISO country code for the address. |
| `data.attributes.phone` | body | `string` | yes | The phone number for the address contact. |
| `data.attributes.email` | body | `string` | no | The email address for the address contact. |
| `data.attributes.notes` | body | `string` | no | Additional notes for the address. |
