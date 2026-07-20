# Utilities - Calculate Date with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/CalculateDate`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Calculate Date](https://support.encodian.com/hc/en-gb/articles/11311253860508)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | yes | The date value to calculate |
| `measurement` | body | `string` | yes | Set the time measurement used for the calculation Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`. |
| `operation` | body | `string` | yes | Set the operation type, either add or subtract Accepted values: `0`, `1`. |
| `interval` | body | `number` | yes | Set amount of time to add or subtract from the 'Date' value provided |
| `daysToExclude` | body | `string` | no | Specify the days to be excluded from the calculation as a comma-delimited list, for example: Saturday, Sunday |
| `datesToExclude` | body | `string` | no | Specify the dates to be excluded from the calculation as a comma-delimited list, for example: 25/12/2024,26/12/2024 |
| `cultureName` | body | `string` | no | Change the thread culture used to process the request. |
