# List Bill Subjects with Congress.gov

Retrieves subjects for a bill from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/bill/:congress/:billType/:billNumber/subjects`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Bill Subjects](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
| `billType` | path | `string` | yes | The bill type. Values include hr, s, hjres, sjres, hconres, sconres, hres, or sres. |
| `billNumber` | path | `number` | yes | The bill's assigned number. For example, 3076. |
