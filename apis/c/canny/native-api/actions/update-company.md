# Update Company with Canny

Updates an existing company in Canny.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/companies/update`
- **Base URL:** `https://canny.io/api`
- **Official documentation:** [Update Company](https://developers.canny.io/api-reference#update_company)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | body | `string` | yes |
| `name` | body | `string` | no |
| `customFields` | body | `object` | no |
| `monthlySpend` | body | `number` | no |
| `created` | body | `date` | no |
