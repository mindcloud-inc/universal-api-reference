# Format Date and Time with 1001fx

Formats a date and time into a specified output format.

## Endpoint

- **Method:** `POST`
- **Path:** `/datetime/formatdatetime`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Format Date and Time](https://1001fx.com/functions/formatdatetime)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `date` | body | `string` | yes | Date value to format. |
| `format` | body | `string` | yes | Target date format. |
| `formatsToTest[]` | body | `array` | no | Candidate input formats to test before formatting. |
