# Update Company with CATS

Updates an existing company in CATS.

## Endpoint

- **Method:** `PUT`
- **Path:** `/companies/:id`
- **Base URL:** `https://api.catsone.com/v3`
- **Official documentation:** [Update Company](https://docs.catsone.com/api/v3/#companies-update-a-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The ID of the company to update. |
| `name` | body | `string` | yes | The company name. |
| `owner_id` | body | `number` | yes | The owning user ID. |
