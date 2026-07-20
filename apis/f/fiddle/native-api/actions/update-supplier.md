# Update Supplier with Fiddle

Updates an existing supplier in Fiddle.

## Endpoint

- **Method:** `PUT`
- **Path:** `/supplier/:supplierId`
- **Base URL:** `https://fiddle.io/rest/api/v2`
- **Official documentation:** [Update Supplier](https://fiddle.io/rest/api/v2/docs/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accountRef` | body | `string` | no | Account reference |
| `address` | body | `string` | no | Supplier address line 1 |
| `address2` | body | `string` | no | Supplier address line 2 |
| `city` | body | `string` | no | Supplier city |
| `country` | body | `string` | no | Supplier country |
| `email` | body | `string` | no | Supplier email |
| `fax` | body | `string` | no | Supplier fax |
| `mobile` | body | `string` | no | Supplier mobile |
| `notes` | body | `string` | no | Supplier notes |
| `paymentInfo` | body | `string` | no | Payment info |
| `paymentTerms` | body | `string` | no | Payment terms |
| `phone` | body | `string` | no | Supplier phone |
| `state` | body | `string` | no | Supplier state |
| `supplierId` | path | `string` | yes | Supplier ID |
| `zip` | body | `string` | no | Supplier ZIP or postal code |
| `name` | body | `string` | yes | Supplier name |
| `disabled` | body | `boolean` | no | Whether the supplier is disabled |
