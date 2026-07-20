# List Summaries By Congress And Bill Type with Congress.gov

Retrieves bill summaries by Congress and bill type in Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/summaries/:congress/:billType`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Summaries By Congress And Bill Type](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/SummariesEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
| `billType` | path | `string` | yes | The bill type. Values include hr, s, hjres, sjres, hconres, sconres, hres, or sres. |
