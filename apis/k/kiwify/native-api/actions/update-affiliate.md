# Update Affiliate with Kiwify

Updates an existing affiliate in Kiwify.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/affiliates/:id`
- **Base URL:** `https://public-api.kiwify.com`
- **Official documentation:** [Update Affiliate](https://docs.kiwify.com.br/api-reference/affiliates/edit)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `string` | yes |
| `commission` | body | `number` | no |
| `status` | body | `string` | no |
