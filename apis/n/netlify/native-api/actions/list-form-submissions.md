# List Form Submissions with Netlify

## Endpoint

- **Method:** `GET`
- **Path:** `/forms/:form_id/submissions`
- **Base URL:** `https://api.netlify.com/api/v1`
- **Official documentation:** [List Form Submissions](https://open-api.netlify.com/#operation/listFormSubmissions)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `form_id` | path | `string` | yes |
