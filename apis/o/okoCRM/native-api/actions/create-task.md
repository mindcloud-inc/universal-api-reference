# Create task with OkoCRM

Creates a new task in OkoCRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/`
- **Base URL:** `https://api.okocrm.com/v2`
- **Official documentation:** [Create task](https://okocrm.com/api/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `company_id` | body | `number` | no | Company ID to attach the task to. |
| `contact_id` | body | `number` | no | Contact ID to attach the task to. |
| `executor_id` | body | `number` | yes | The user assigned to the task. |
| `lead_id` | body | `number` | no | Deal ID to attach the task to. Provide one of deal, contact, or company. |
| `text` | body | `string` | no | Task text. Provide this or a task type ID. |
| `type_id` | body | `number` | no | Task type ID. |
