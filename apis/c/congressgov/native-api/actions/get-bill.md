# Get Bill with Congress.gov

Retrieves a bill from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/bill/:congress/:billType/:billNumber`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [Get Bill](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
| `billType` | path | `string` | yes | The bill type. Values include hr, s, hjres, sjres, hconres, sconres, hres, or sres. |
| `billNumber` | path | `number` | yes | The bill's assigned number. For example, 3076. |
