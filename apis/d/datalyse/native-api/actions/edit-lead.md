# Edit Lead with Datalyse

Updates an existing contact or company in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/leads/edit.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Edit Lead](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | no | Set to "unassigned" to assign this lead to all agents, or provide a specific agent_id to assign it to an agent (optional) |
| `country` | body | `string` | no | Country ISO code |
| `email` | body | `string` | no | Email |
| `lastname` | body | `string` | no | Last name |
| `lead_id` | body | `string` | yes | ID of the contact or company to edit |
| `name` | body | `string` | no | Name of the contact or company |
| `phone` | body | `string` | no | Phone number with international prefix |
| `status` | body | `string` | no | Status ID |
