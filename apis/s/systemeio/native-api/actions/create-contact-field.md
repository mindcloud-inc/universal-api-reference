# Create Contact Field with Systeme.io

Creates a contact field in Systeme.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/contact_fields`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Create Contact Field](https://developer.systeme.io/reference/api_contact_fields_post-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldName` | body | `string` | yes | Name of the contact field |
| `slug` | body | `string` | yes | Unique slug for the contact field |
