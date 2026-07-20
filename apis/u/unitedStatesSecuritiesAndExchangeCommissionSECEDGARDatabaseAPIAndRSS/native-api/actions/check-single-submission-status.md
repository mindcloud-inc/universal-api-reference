# Check Single Submission Status with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves the status of a single EDGAR submission.

## Endpoint

- **Method:** `GET`
- **Path:** `https://api.edgarfiling.sec.gov/submission/[:accessionNumber]/status`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Check Single Submission Status](https://api.edgarfiling.sec.gov/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessionNumber` | path | `string` | yes | EDGAR accession number to check. |
