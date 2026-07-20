# List Bills By Congress And Type with Congress.gov

Retrieves bills by Congress and bill type in Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/bill/:congress/:billType`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Bills By Congress And Type](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/BillEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
| `billType` | path | `string` | yes | The bill type. Values include hr, s, hjres, sjres, hconres, sconres, hres, or sres. |
