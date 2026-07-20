# Get Client Data By Field with CoachAccountable

Retrieves client data by field from CoachAccountable.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://www.coachaccountable.com/API`
- **Official documentation:** [Get Client Data By Field](https://www.coachaccountable.com/APIDocs#ClientData.getByField)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fieldname` | body | `string` | yes | The name of the field to be fetched, either input name within a Form-based Worksheet, Metric name, or fedBy input name for a Metric. |
| `ClientID` | body | `number` | no | The ID of the client for whom data is to be returned, if desired only for a single, specific client. |
| `dateFrom` | body | `date` | no | Set to restrict data returned to those dated at or after the provided value. |
| `dateTo` | body | `date` | no | Set to restrict data returned to those dated at or before the provided value. |
| `includeInactive` | body | `boolean` | no | Include data for Clients who are inactive. |
| `dateBucket` | body | `list` | no | Group data dates to into weeks or months for a more coherent spreadsheet. Useful when, for example, clients all report on a weekly basis yet might do it on any day of the week. Accepted values: `D`, `M`, `W`. |
| `whatData` | body | `list` | no | Data points often have a sensible textual and numeric value. Set this to get one, the other, or both. Accepted values: `B`, `N`, `T`. |
| `structure` | body | `list` | no | How should the returned data be structured in the CSV? Date Grid means each row is a client, and columns are dates of the data. Data Point Listing returns rows that are each a single data point: ClientID, client name, date, and value. Accepted values: `D`, `L`. |
