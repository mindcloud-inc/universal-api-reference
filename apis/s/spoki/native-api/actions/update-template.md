# Update Template with Spoki

Updates an existing WhatsApp template by ID with partial changes.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/templates/{{id}}/`
- **Base URL:** `https://api.spoki.com/api/1`
- **Official documentation:** [Update Template](https://documenter.getpostman.com/view/21611004/UzBqnPvF)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The template ID. |
| `payload` | body | `object` | yes | Template fields to update, using Spoki's template schema. |
