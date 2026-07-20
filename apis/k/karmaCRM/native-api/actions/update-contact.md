# Update Contact with Karma CRM

Updates an existing contact in Karma CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v3/contacts/:id.json`
- **Base URL:** `https://app.karmacrm.com`
- **Official documentation:** [Update Contact](https://docs.karmacrm.com/#update-a-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the contact to update. |
| `contact` | body | `object` | yes | Contact payload object with the fields to update. |
