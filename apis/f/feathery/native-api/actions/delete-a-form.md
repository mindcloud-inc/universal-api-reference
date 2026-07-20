# Delete a Form with Feathery

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/form/:form_id/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Delete a Form](https://api-docs.feathery.io/#delete-a-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_id` | path | `string` | yes | The ID of the form to delete. |
| `confirm_delete` | body | `boolean` | yes | Set to true to confirm deletion of the form. |
