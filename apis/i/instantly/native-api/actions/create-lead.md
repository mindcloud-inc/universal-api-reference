# Create Lead with Instantly

Creates a new lead in Instantly.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/leads`
- **Base URL:** `https://api.instantly.ai`
- **Official documentation:** [Create Lead](https://developer.instantly.ai/api-reference/lead/create-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `list_id` | body | `string` | yes | Lead list ID associated with the lead. |
| `email` | body | `string` | yes | Email address of the lead. |
| `first_name` | body | `string` | no | First name of the lead. |
| `last_name` | body | `string` | no | Last name of the lead. |
