# Create Lead with Datalyse

Creates a new contact or company in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/leads/create.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Create Lead](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `add_note` | body | `string` | no | Add a note to this contact or company (optional) |
| `agent_id` | body | `string` | no | Set to "unassigned" to assign this lead to all agents, or provide a specific agent_id to assign it to an agent (optional) |
| `country` | body | `string` | no | Country ISO code |
| `email` | body | `string` | no | Email |
| `ESCOMPANIES` | body | `string` | no | Set to "y" if it is a company (optional) |
| `in_leadcompany` | body | `string` | no | ID of the company this contact belongs to (optional) |
| `lastname` | body | `string` | no | Last name |
| `leadtypedatal` | body | `string` | no | Identifier of the contact or company type (optional) |
| `name` | body | `string` | yes | Name for the contact |
| `phone` | body | `string` | no | Phone with international prefix |
| `status` | body | `string` | no | Status ID |
