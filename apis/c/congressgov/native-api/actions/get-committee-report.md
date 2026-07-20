# Get Committee Report with Congress.gov

Retrieves a committee report from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/committee-report/:congress/:reportType/:reportNumber`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [Get Committee Report](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteeReportEndpoint.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
| `reportType` | path | `string` | yes | The committee report type. Values include hrpt, srpt, or erpt. |
| `reportNumber` | path | `number` | yes | The committee report's assigned number. For example, 617. |
