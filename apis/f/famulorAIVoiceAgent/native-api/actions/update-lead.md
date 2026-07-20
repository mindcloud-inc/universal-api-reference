# Update Lead with Famulor AI - Voice Agent

Updates an existing lead in Famulor.

## Endpoint

- **Method:** `PUT`
- **Path:** `/user/leads/:id`
- **Base URL:** `https://app.famulor.de/api`
- **Official documentation:** [Update Lead](https://docs.famulor.io/en/api-reference/leads/update)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `number` | no | Updated campaign ID for the lead. |
| `id` | path | `number` | yes | Famulor lead ID. |
| `phone_number` | body | `string` | no | Updated lead phone number. |
| `status` | body | `string` | no | Updated lead status. |
| `variables` | body | `object` | no | Variables to merge into the lead. |
