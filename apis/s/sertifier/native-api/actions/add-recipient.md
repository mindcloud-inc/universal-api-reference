# Add Recipient with Sertifier

Creates a new recipient in Sertifier.

## Endpoint

- **Method:** `POST`
- **Path:** `/recipient`
- **Base URL:** `https://b2b.sertifier.com`
- **Official documentation:** [Add Recipient](https://sertifier.docs.apiary.io/reference/recipient/add-update-recipient)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `recipients[].name` | body | `string` | yes |
| `recipients[].email` | body | `string` | yes |
