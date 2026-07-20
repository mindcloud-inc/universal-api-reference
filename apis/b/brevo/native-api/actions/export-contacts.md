# Export Contacts with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/contacts/export`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Export Contacts](https://developers.brevo.com/reference/request-contact-export)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `customContactFilter` | body | `object` | yes | Filter object for selecting contacts to export. |
| `email` | body | `string` | yes | Email address to receive the exported contacts file. |
