# Create Opportunity with Datalyse

Creates a new opportunity in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/opportunities/create.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Create Opportunity](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | no | Agent ID (optional) |
| `amount` | body | `string` | yes | Total amount |
| `calendar_id` | body | `string` | no | Calendar task ID (optional) |
| `currency` | body | `string` | yes | Currency |
| `description` | body | `string` | yes | Description of the opportunity |
| `expecteddate` | body | `string` | no | Expected closing date (optional) |
| `lead_id` | body | `string` | yes | ID of the contact or company |
| `pipeline` | body | `string` | no | Pipeline ID (optional) |
| `status` | body | `string` | no | Status ID |
| `statusd` | body | `string` | no | Stage (optional) |
| `time` | body | `string` | no | Time (optional) |
