# Update CRM Contact with WhatsScale

Updates an existing CRM contact in WhatsScale.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/crm/contacts/:id`
- **Base URL:** `https://proxy.whatsscale.com`
- **Official documentation:** [Update CRM Contact](https://whatsscale.com/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | CRM contact ID. |
| `name` | body | `string` | no | Optional updated display name. |
| `tags[]` | body | `array<string>` | no | Optional replacement tag list. Send multiple values as a array. |
