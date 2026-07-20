# List Actions with SafetyCulture

Retrieves actions from SafetyCulture.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/v1/actions/list`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [List Actions](https://developer.safetyculture.com/reference/actionsservice_getactions)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | body | `number` | no | Optional. Number of actions to be returned in a single request. Maximum 100. Non-positive values are ignored. The presence of `next_page_token` in the response indicates that more results might be available. For example: '20'. |
| `page_token` | body | `string` | no | Optional. If present, then retrieve the next batch of results from the preceding call to this method. `page_token` must be the value of `next_page_token` from the previous response.  The values of other method parameters should be identical to those in the previous call. For example: 'ODFBMzQ3MDYtNzQxNy00RDZGLThDNjE1MEFDMkM4MTQ3NDQ='. |
| `inspection_id` | body | `string` | no | Optional. The ID of the inspection the action belongs to. Deprecated, inspectionID in `filters` should be used instead. |
| `offset` | body | `number` | no | Optional. Offset from where on the actions will be listed. |
| `sort_field` | body | `string` | no | Optional. Which field to use for sorting. |
| `sort_direction` | body | `string` | no | Optional. Direction for sorting. |
| `without_count` | body | `boolean` | no | Optional. If true, will not return the count of actions. |
| `task_filters[]` | body | `array<object>` | no | Optional. The array of filters to apply in your request. You can apply multiple filters in a single request. |
