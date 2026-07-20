# List Issues with SafetyCulture

Retrieves issues from SafetyCulture.

## Endpoint

- **Method:** `POST`
- **Path:** `/tasks/v1/incidents/list`
- **Base URL:** `https://api.safetyculture.io`
- **Official documentation:** [List Issues](https://developer.safetyculture.com/reference/incidentsservice_getincidents)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `page_size` | body | `number` | no | Optional. Number of issues to be returned in a single request. This must be a value between 1 and 100, any values outside of this range will be ignored. The presence of `next_page_token` in the response indicates that more results might be available. |
| `page_token` | body | `string` | no | Optional. If present, then retrieve the next batch of results from the preceding call to this method. `page_token` must be the value of `next_page_token` from the previous response.  The values of other method parameters should be identical to those in the previous call. This can be used to retrieve more than 100 issues with multiple API calls. For example: 'ODFBMzQ3MDYtNzQxNy00RDZGLThDNjE1MEFDMkM4MTQ3NDQ=' |
| `sort_field` | body | `string` | no | Optional. Which field to use for sorting. |
| `sort_direction` | body | `string` | no | Optional. Direction for sorting. |
| `filters[]` | body | `array<object>` | no | Optional. An array of filters can be provided in the request to filter the issues. |
