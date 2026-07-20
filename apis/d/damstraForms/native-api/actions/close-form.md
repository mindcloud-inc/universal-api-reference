# Close Form with Damstra Forms

Closes a form in Damstra Forms.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/forms/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Close Form](https://sammapi.docs.apiary.io/#reference/forms/form-instance/close-a-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Path parameter id. |
| `submitter_user_id` | body | `string` | yes | User identifier for the person closing the form. |
| `lock_version` | body | `number` | yes | Current lock version for optimistic concurrency control. |
