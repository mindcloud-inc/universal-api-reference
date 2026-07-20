# Create Contact with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/contacts`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Create Contact](https://developers.brevo.com/reference/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Contact email address. |
| `updateEnabled` | body | `boolean` | no | Update existing contact if it already exists. |
