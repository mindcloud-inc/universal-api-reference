# List Members By Congress with Congress.gov

Retrieves members for a specific Congress in Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/member/congress/:congress`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Members By Congress](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/MemberEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `congress` | path | `number` | yes | The congress number. For example, 118. |
