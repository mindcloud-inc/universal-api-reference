# List CRS Reports with US Congress CRS

Retrieves CRS reports from US Congress CRS.

## Endpoint

- **Method:** `GET`
- **Path:** `/crsreport`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List CRS Reports](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CRSReportEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromDateTime` | query | `date` | no | Starting timestamp to filter CRS reports by update date. Use ISO timestamp format such as 2026-01-01T00:00:00Z. |
| `toDateTime` | query | `date` | no | Ending timestamp to filter CRS reports by update date. Use ISO timestamp format such as 2026-05-05T00:00:00Z. |
