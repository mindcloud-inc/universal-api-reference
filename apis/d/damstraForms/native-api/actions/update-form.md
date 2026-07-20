# Update Form with Damstra Forms

Updates a form in Damstra Forms.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/forms/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Form](https://sammapi.docs.apiary.io/#reference/forms/form-instance/update-a-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Path parameter id. |
| `submitter_user_id` | body | `string` | yes | User identifier for the person submitting the update. |
| `lock_version` | body | `number` | yes | Current lock version for optimistic concurrency control. |
| `fields[]` | body | `array<object>` | yes | Field values to update, using Damstra field_reference values. |
