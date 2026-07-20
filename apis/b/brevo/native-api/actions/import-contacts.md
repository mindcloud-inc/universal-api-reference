# Import Contacts with Brevo

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/contacts/import`
- **Base URL:** `https://api.brevo.com`
- **Official documentation:** [Import Contacts](https://developers.brevo.com/reference/import-contacts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fileUrl` | body | `string` | no | Public URL to CSV file for contact import. |
| `jsonBody` | body | `object` | no | Array of contact objects to import. |
| `listIds` | body | `object<number>` | no | List IDs where imported contacts should be added. |
| `updateExistingContacts` | body | `boolean` | no | Update existing contacts when they already exist. |
