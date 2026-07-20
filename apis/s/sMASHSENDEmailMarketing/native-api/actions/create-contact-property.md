# Create Contact Property with SMASHSEND Email Marketing

Creates a new contact property in SMASHSEND.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/contact-properties`
- **Base URL:** `https://api.smashsend.com`
- **Official documentation:** [Create Contact Property](https://smashsend.com/docs/api/contact-properties)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | Optional description of the contact property. |
| `displayName` | body | `string` | yes | Human-readable name for the contact property. |
| `type` | body | `string` | yes | Property type such as STRING, TEXT, EMAIL, URL, PHONE, DATE, NUMBER, INTEGER, or BOOLEAN. |
| `typeConfig` | body | `object` | no | Optional type configuration object for the property. |
