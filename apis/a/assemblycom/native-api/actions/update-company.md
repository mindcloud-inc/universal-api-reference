# Update Company with Assembly.com

Updates an existing company in Assembly.com.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/companies/:id`
- **Base URL:** `https://api.assembly.com/v1`
- **Official documentation:** [Update Company](https://docs.assembly.com/reference/update-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the company to be updated. |
| `name` | body | `string` | no | The company’s new name. |
| `customFields` | body | `object` | no | Optional custom field updates keyed by Assembly custom field keys. |
