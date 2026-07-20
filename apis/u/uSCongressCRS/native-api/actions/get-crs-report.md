# Get CRS Report with US Congress CRS

Retrieves a CRS report from US Congress CRS.

## Endpoint

- **Method:** `GET`
- **Path:** `/crsreport/:reportNumber`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [Get CRS Report](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CRSReportEndpoint.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reportNumber` | path | `string` | yes | CRS report ID or number, such as R47175 or IF13211. |
