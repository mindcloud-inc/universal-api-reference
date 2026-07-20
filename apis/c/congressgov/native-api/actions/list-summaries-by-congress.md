# List Summaries By Congress with Congress.gov

Retrieves bill summaries from a specific Congress in Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/summaries/:congress`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Summaries By Congress](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/SummariesEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
