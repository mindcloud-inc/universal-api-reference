# Run Category Action with Shuffler

Creates a category action run in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/apps/categories/run`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Run Category Action](https://shuffler.io/docs/API#shufflepy)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `app_name` | body | `string` | yes | App name. |
| `category` | body | `string` | yes | Category name. |
| `fields[]` | body | `array` | no | Field payload array. |
| `label` | body | `string` | yes | Action label. |
| `skip_workflow` | body | `boolean` | no | Skip workflow execution. |
