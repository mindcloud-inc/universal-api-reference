# Assign Lead with noCRM.io

Assigns a lead in noCRM.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:id/assign`
- **Base URL:** `{baseUrl}/api/v2`
- **Official documentation:** [Assign Lead](https://www.nocrm.io/api#assign-a-lead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The identifier of the lead. |
| `user_id` | body | `string` | yes | User ID or email to assign the lead to. |
