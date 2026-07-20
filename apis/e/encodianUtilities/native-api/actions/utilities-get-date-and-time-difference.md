# Utilities - Get Date and Time Difference with Encodian - Utilities

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/Utilities/GetDateTimeDifference`
- **Base URL:** `https://api.apps-encodian.com`
- **Official documentation:** [Utilities - Get Date and Time Difference](https://support.encodian.com/hc/en-gb/articles/11753070117661)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `startDateTime` | body | `string` | yes | Start date (and optionally time) of the period to be calculated |
| `endDateTime` | body | `string` | yes | End date (and optionally time) of the period to be calculated |
| `interval` | body | `string` | yes | The interval to calculate - Year, Quarter, Month, Week, Day, Hour, Minute, Second, Millisecond Accepted values: `0`, `1`, `2`, `3`, `4`, `5`, `6`, `7`, `8`. |
| `daysToExclude` | body | `string` | no | Specify the days to be excluded from the calculation as a comma-delimited list, for example: Saturday, Sunday |
| `cultureName` | body | `string` | no | Change the thread culture used to process the request. |
