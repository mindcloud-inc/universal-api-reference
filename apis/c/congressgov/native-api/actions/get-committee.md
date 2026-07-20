# Get Committee with Congress.gov

Retrieves a committee from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/committee/:chamber/:committeeCode`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [Get Committee](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteeEndpoint.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chamber` | path | `string` | yes | The chamber name. Values include house, senate, or joint. |
| `committeeCode` | path | `string` | yes | The committee code. For example, hspw00. |
