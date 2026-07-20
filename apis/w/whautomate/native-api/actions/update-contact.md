# Update Contact with Whautomate

Updates an existing contact in Whautomate.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/contacts/{{contactId}}`
- **Base URL:** `https://api.whautomate.com`
- **Official documentation:** [Update Contact](https://help.whautomate.com/product-guides/whautomate-rest-api/contacts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `channel` | body | `string` | no |
| `contactId` | path | `string` | yes |
| `customFields` | body | `object` | no |
| `location` | body | `object` | no |
| `name` | body | `string` | no |
| `notes` | body | `string` | no |
| `phoneNumber` | body | `string` | no |
| `tags[]` | body | `array<string>` | no |
