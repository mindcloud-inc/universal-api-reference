# Add Contact with Whautomate

Creates a new contact in Whautomate.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contacts`
- **Base URL:** `https://api.whautomate.com`
- **Official documentation:** [Add Contact](https://help.whautomate.com/product-guides/whautomate-rest-api/contacts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `customFields` | body | `object` | no |
| `location` | body | `object` | yes |
| `name` | body | `string` | yes |
| `notes` | body | `string` | no |
| `phoneNumber` | body | `string` | yes |
| `tags[]` | body | `array<string>` | no |
