# Create Vendor with Invoice Ninja

## Endpoint

- **Method:** `POST`
- **Path:** `/vendors`
- **Base URL:** `https://invoicing.co/api/v1`
- **Official documentation:** [Create Vendor](https://api-docs.invoicing.co/#tag/vendors/operation/storeVendor)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The vendor name. |
| `email` | body | `string` | no | Primary vendor email. |
| `phone` | body | `string` | no | Primary vendor phone number. |
