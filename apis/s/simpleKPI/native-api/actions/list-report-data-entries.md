# List Report Data Entries with SimpleKPI

Retrieves report data entries from SimpleKPI.

## Endpoint

- **Method:** `GET`
- **Path:** `reports/AllDataEntries`
- **Base URL:** `https://{subdomain}.simplekpi.com/api/`
- **Official documentation:** [List Report Data Entries](https://support.simplekpi.com/Developers/Reports)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `fromDate` | query | `string` | no | Optional report start date. |
| `toDate` | query | `string` | no | Optional report end date. |
