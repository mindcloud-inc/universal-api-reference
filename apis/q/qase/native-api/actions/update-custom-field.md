# Update Custom Field with Qase

Updates an existing custom field in Qase.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/custom_field/:id`
- **Base URL:** `https://api.qase.io/v1`
- **Official documentation:** [Update Custom Field](https://developers.qase.io/reference/get-projects)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Identifier. |
| `title` | body | `string` | yes | Required request field title. |
