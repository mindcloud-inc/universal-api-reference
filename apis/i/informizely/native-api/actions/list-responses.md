# List Responses with Informizely

## Endpoint

- **Method:** `GET`
- **Path:** `/responses`
- **Base URL:** `https://api.informizely.com/api/v1`
- **Official documentation:** [List Responses](https://www.informizely.com/help/report-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The ID of the survey whose responses you want to retrieve. |
| `fromDate` | query | `date` | no | The earliest UTC timestamp to include, in ISO 8601 format. |
| `toDate` | query | `date` | no | The latest UTC timestamp to include, in ISO 8601 format. |
| `fromIndex` | query | `number` | no | The zero-based start index after any date filtering is applied. |
| `toIndex` | query | `number` | no | The zero-based end index after any date filtering is applied. |
| `includeRemoved` | query | `boolean` | no | Keep this true to include data for removed questions. |
| `includeEmpty` | query | `boolean` | no | Keep this true to include empty answers. |
| `excludeQuestions` | query | `boolean` | no | Set to true to omit question metadata from the response payload. |
