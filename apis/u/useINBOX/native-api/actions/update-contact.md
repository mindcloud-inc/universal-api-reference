# Update Contact with UseINBOX

Updates an existing contact in UseINBOX.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/v1/contacts/:id`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Update Contact](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Contact ID from INBOX. |
| `tags[]` | body | `array<string>` | no | Tags to apply to the contact. Send multiple values as a array. |
| `customFields[].customFieldId` | body | `string` | no | Custom field ID to update for the contact. |
| `customFields[].value` | body | `string` | no | Custom field value for the contact. |
