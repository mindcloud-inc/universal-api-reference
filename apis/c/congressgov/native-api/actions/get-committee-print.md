# Get Committee Print with Congress.gov

Retrieves a committee print from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/committee-print/:congress/:chamber/:jacketNumber`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [Get Committee Print](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteePrintEndpoint.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
| `chamber` | path | `string` | yes | The chamber name. Values include house, senate, or joint. |
| `jacketNumber` | path | `number` | yes | The jacket number for the print. For example, 48144. |
