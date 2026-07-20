# Edit Company with Datalyse

Updates an existing company in Datalyse.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/1.0/companies/edit.json`
- **Base URL:** `https://api.datalyse.io`
- **Official documentation:** [Edit Company](https://developers.datalyse.io/devs/content_api.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `agent_id` | body | `string` | no | Agent ID or "unassigned" (optional) |
| `company_lead_id` | body | `string` | yes | ID of the company to edit |
| `country` | body | `string` | no | Country ISO code (optional) |
| `email` | body | `string` | no | Email (optional) |
| `name` | body | `string` | no | Company name (optional) |
| `phone` | body | `string` | no | Phone number with international prefix (optional) |
| `status` | body | `string` | no | Status ID (optional) |
