# Get Timesheet with HR Partner

## Endpoint

- **Method:** `GET`
- **Path:** `/singletimesheet`
- **Base URL:** `https://api.hrpartner.io`
- **Official documentation:** [Get Timesheet](https://developer.hrpartner.io/#get-a-single-timesheet)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `employee` | query | `string` | yes | Employee code to fetch a single timesheet for. |
| `sequence` | query | `string` | yes | Exact timesheet sequence label, such as Mon, 01 Jan 2024 to Sun, 07 Jan 2024. |
