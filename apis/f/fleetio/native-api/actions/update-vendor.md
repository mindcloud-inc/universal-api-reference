# Update Vendor with Fleetio

Updates an existing vendor in Fleetio.

## Endpoint

- **Method:** `PATCH`
- **Path:** `vendors/:id`
- **Base URL:** `https://secure.fleetio.com/api/`
- **Official documentation:** [Update Vendor](https://developer.fleetio.com/docs/api/vendors-update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The id of the relevant record |
| `name` | body | `string` | no | The name of the Vendor. Must be unique. |
| `city` | body | `string` | no | The city of the Vendor. |
| `contact_email` | body | `string` | no | The email address of the contact person for the Vendor. |
| `contact_name` | body | `string` | no | The name of the contact person for the Vendor. |
| `contact_phone` | body | `string` | no | The phone number of the contact person for the Vendor. |
| `country` | body | `string` | no | The country of the Vendor. |
| `external_id` | body | `string` | no | An external ID for the Vendor. Must be unique. |
| `phone` | body | `string` | no | The phone number of the Vendor. |
| `postal_code` | body | `string` | no | The postal code or ZIP code of the Vendor. |
| `region` | body | `string` | no | The region, state, province, or territory of the Vendor. |
| `street_address` | body | `string` | no | The street address of the Vendor. |
| `street_address_line_2` | body | `string` | no | The second line of the street address of the Vendor. |
| `website` | body | `string` | no | The website of the Vendor. |
| `fuel` | body | `boolean` | no | Indicates whether the Vendor provides fuel. Will be able to be listed on `Fuel Entries`. |
| `service` | body | `boolean` | no | Indicates whether the Vendor provides service. This Vendor will be able to be listed on `Service Entries` and `Work Orders`. |
| `parts` | body | `boolean` | no | Indicates whether the Vendor provides parts. This Vendor will be able to be listed on `Parts` and `Purchase Orders`. |
| `vehicle` | body | `boolean` | no | Indicates whether the Vendor provides vehicles. This Vendor will be able to be listed on `Acquisitions` and `Vehicles`. |
| `custom_fields` | body | `object` | no | *Full details on working with Custom Fields [here](/docs/overview/custom-fields). |
