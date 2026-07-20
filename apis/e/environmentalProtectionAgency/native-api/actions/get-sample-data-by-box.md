# Get Sample Data By Box with Environmental Protection Agency

Retrieves sample data for a bounding box from EPA AQS.

## Endpoint

- **Method:** `GET`
- **Path:** `/sampleData/byBox`
- **Base URL:** `https://aqs.epa.gov/data/api`
- **Official documentation:** [Get Sample Data By Box](https://aqs.epa.gov/aqsweb/documents/data_api.html#sample-data)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `param` | query | `string` | yes | AQS parameter code. EPA allows up to five comma-separated 5-digit parameter codes for most data services. Send multiple values as a string separated by `,`. |
| `bdate` | query | `string` | yes | Begin date in YYYYMMDD format. |
| `edate` | query | `string` | yes | End date in YYYYMMDD format. EPA requires this to be in the same year as the begin date except for monitors. |
| `minlat` | query | `number` | yes | Southern latitude bound for a geographic box query. |
| `maxlat` | query | `number` | yes | Northern latitude bound for a geographic box query. |
| `minlon` | query | `number` | yes | Western longitude bound for a geographic box query. Use negative values in the western hemisphere. |
| `maxlon` | query | `number` | yes | Eastern longitude bound for a geographic box query. Use negative values in the western hemisphere. |
| `duration` | query | `string` | no | Optional one-character AQS sample duration code for sample data requests. |
| `cbdate` | query | `string` | no | Optional begin date in YYYYMMDD format for filtering by date of last change. |
| `cedate` | query | `string` | no | Optional end date in YYYYMMDD format for filtering by date of last change. |
