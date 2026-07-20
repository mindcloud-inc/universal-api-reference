# List Committee Bills with Congress.gov

Retrieves bills for a committee from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/committee/:chamber/:committeeCode/bills`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Committee Bills](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/CommitteeEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `chamber` | path | `string` | yes | The chamber name. Values include house, senate, or joint. |
| `committeeCode` | path | `string` | yes | The committee code. For example, hspw00. |
