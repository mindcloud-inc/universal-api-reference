# Update Action with Damstra Forms

Updates an action in Damstra Forms.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/actions/{id}`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Update Action](https://sammapi.docs.apiary.io/#reference/actions/action-instance/update-an-action)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | The unique identifier of the action. |
| `submitter_user_id` | body | `string` | yes | User identifier for the person submitting the update. |
| `lock_version` | body | `number` | yes | Current lock version for optimistic concurrency control. |
| `fields[]` | body | `array<object>` | yes | Field values to update, using Damstra field_reference values. |
