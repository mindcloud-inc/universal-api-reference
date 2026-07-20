# Copy a Form with Feathery

## Endpoint

- **Method:** `POST`
- **Path:** `/api/form/copy/`
- **Base URL:** `https://api.feathery.io`
- **Official documentation:** [Copy a Form](https://api-docs.feathery.io/#copy-a-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_name` | body | `string` | yes | The name of the new copied form. |
| `copy_form_id` | body | `string` | yes | The ID of the form to copy. |
