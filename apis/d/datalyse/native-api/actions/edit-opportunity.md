# Edit Opportunity with Datalyse

Updates an existing opportunity in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/opportunities/edit.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Edit Opportunity](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | no | Agent ID or "unassigned" (optional) |
| `amount` | body | `string` | no | Total amount (optional) |
| `currency` | body | `string` | no | Currency (optional) |
| `description` | body | `string` | no | Description of the opportunity (optional) |
| `opportunity_id` | body | `string` | yes | ID of the opportunity to edit |
| `pipeline` | body | `string` | no | Pipeline ID (optional) |
| `status` | body | `string` | no | Status ID (optional) |
