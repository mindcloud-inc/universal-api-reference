# Add Contact with Wati

Creates a new contact in Wati.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/addContact/:whatsappNumber`
- **Base URL:** `{apiEndpointUrl}`
- **Official documentation:** [Add Contact](https://docs.wati.io/reference/post_api-v1-addcontact-whatsappnumber)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `whatsappNumber` | path | `string` | yes | Target WhatsApp phone number for the contact. |
| `name` | body | `string` | yes | Display name for the contact. |
| `customParams[]` | body | `array<object>` | no | Custom attributes to store on the contact. |
