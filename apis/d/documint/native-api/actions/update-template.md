# Update Template with Documint

Updates an existing template in Documint.

## Endpoint

- **Method:** `PUT`
- **Path:** `/templates/:id`
- **Base URL:** `https://api.documint.me/1`
- **Official documentation:** [Update Template](https://documenter.getpostman.com/view/11741160/TVK5cLxQ)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Documint template ID to update. |
| `name` | body | `string` | yes | Updated name for the template. |
