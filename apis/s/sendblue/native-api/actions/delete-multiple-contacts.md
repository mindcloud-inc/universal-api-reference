# Delete Multiple Contacts with Sendblue

Deletes multiple contacts from Sendblue.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/v2/contacts`
- **Base URL:** `https://api.sendblue.co`
- **Official documentation:** [Delete Multiple Contacts](https://docs.sendblue.com/api/resources/contacts/subresources/bulk/methods/delete/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_ids[]` | body | `array<string>` | yes | Array of phone numbers in E.164 format to delete. |
