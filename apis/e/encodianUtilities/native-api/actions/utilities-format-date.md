# Utilities - Format Date with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/FormatDate`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Format Date](https://support.encodian.com/hc/en-gb/articles/11053469626525)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | yes | The date value to format |
| `format` | body | `string` | yes | Set the date format - https://learn.microsoft.com/en-us/dotnet/standard/base-types/custom-date-and-time-format-strings |
| `cultureName` | body | `string` | no | Change the thread culture used to process the request. |
