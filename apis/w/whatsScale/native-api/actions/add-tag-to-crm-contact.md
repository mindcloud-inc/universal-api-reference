# Add Tag to CRM Contact with WhatsScale

Adds a tag to an existing WhatsScale CRM contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/crm/contacts/:id/tags`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Add Tag to CRM Contact](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | CRM contact ID. |
| `tag` | body | `string` | yes | Tag to add. |
