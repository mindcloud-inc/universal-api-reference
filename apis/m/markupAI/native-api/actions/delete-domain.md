# Delete Domain with Markup AI

Deletes an existing terminology domain from Markup AI.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v1/terminology/domains/:domain_id`
- **Base URL:** `https://api.markup.ai`
- **Official documentation:** [Delete Domain](https://docs.markup.ai/api-reference/terminology/delete-domain)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain_id` | path | `string` | yes | UUID of the domain to delete. |
