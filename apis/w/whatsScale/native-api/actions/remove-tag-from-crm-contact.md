# Remove Tag from CRM Contact with WhatsScale

Removes a tag from an existing WhatsScale CRM contact.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/crm/contacts/:id/tags/:tag`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Remove Tag from CRM Contact](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | CRM contact ID. |
| `tag` | path | `string` | yes | Tag to remove. |
