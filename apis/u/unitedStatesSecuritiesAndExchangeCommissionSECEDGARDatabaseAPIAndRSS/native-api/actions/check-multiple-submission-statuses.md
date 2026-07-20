# Check Multiple Submission Statuses with United States Securities and Exchange Commission (SEC) EDGAR Database

Retrieves statuses for multiple EDGAR submissions.

## Endpoint

- **Method:** `POST`
- **Path:** `https://api.edgarfiling.sec.gov/submission/status`
- **Base URL:** `https://www.sec.gov`
- **Official documentation:** [Check Multiple Submission Statuses](https://api.edgarfiling.sec.gov/openapi.json)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `accessionNumbers[]` | body | `array<string>` | yes | Up to 25 EDGAR accession numbers to check. |
