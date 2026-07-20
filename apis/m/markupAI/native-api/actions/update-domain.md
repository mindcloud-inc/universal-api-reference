# Update Domain with Markup AI

Updates an existing terminology domain in Markup AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/terminology/domains/:domain_id`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Update Domain](https://docs.markup.ai/api-reference/terminology/update-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | path | `string` | yes | UUID of the terminology domain to update. |
| `name` | body | `string` | no | Updated domain name. |
| `description` | body | `string` | no | Updated domain description. |
