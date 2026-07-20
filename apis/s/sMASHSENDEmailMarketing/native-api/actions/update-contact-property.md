# Update Contact Property with SMASHSEND Email Marketing

Updates an existing contact property in SMASHSEND.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact-properties/:propertyId`
- **Base URL:** `https://api.smashsend.com`
- **Official documentation:** [Update Contact Property](https://smashsend.com/docs/api/contact-properties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional new description for the property. |
| `displayName` | body | `string` | no | Optional new display name for the property. |
| `propertyId` | path | `string` | yes | The SMASHSEND contact property ID to update. |
| `typeConfig` | body | `object` | no | Optional type configuration object for the property. |
