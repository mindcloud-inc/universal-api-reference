# Get Client Data Activity Stats with CoachAccountable

Retrieves client activity stats from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Get Client Data Activity Stats](https://www.coachaccountable.com/APIDocs#ClientData.getActivityStats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientID` | body | `number` | no | The ID of the client for whom data is to be returned, if desired only for a single, specific client. |
| `GroupID` | body | `number` | no | The ID of the Group for whose client members data is to be returned. |
| `CompanyID` | body | `number` | no | The ID of the Company for whose client members data is to be returned. |
| `EngagementID` | body | `number` | no | The ID of the Engagement for whose client data is to be returned. |
| `dateBucket` | body | `list` | no | Group activity statistics according to your bucket size of choice. Accepted values: `D`, `M`, `Q`, `W`, `Y`. |
| `dateFrom` | body | `date` | no | The lower bound of the date range to report stats on.. |
| `dateTo` | body | `date` | no | The upper bound of the date range to report stats on. |
| `itemTypes` | body | `string` | no | The types of items to be included, each letter signifies a single type. A for Action, M for Metric, P for Appointment, S for Session Note, W for Worksheet, J for Journal Entry, F for File, C for Comment. |
| `includeInactive` | body | `boolean` | no | Include data for Clients who are inactive. |
| `includeTotals` | body | `boolean` | no | Set true to inclue a totals column. |
| `includeAverages` | body | `boolean` | no | Set true to inclue an averages column. |
