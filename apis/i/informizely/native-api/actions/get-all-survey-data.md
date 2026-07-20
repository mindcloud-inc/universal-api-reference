# Get All Survey Data with Informizely

## Endpoint

- **Method:** `GET`
- **Path:** `/all`
- **Base URL:** `https://api.informizely.com/api/v1`
- **Official documentation:** [Get All Survey Data](https://www.informizely.com/help/report-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | query | `string` | yes | The ID of the survey whose full data you want to retrieve. |
| `includeRemoved` | query | `boolean` | no | Keep this true to include data for removed questions. |
| `includeEmpty` | query | `boolean` | no | Keep this true to include empty answers. |
| `excludeQuestions` | query | `boolean` | no | Set to true to omit question metadata from the response payload. |
