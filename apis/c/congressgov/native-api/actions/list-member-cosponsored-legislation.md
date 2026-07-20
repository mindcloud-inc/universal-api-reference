# List Member Cosponsored Legislation with Congress.gov

Retrieves legislation cosponsored by a member in Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/member/:bioguideId/cosponsored-legislation`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [List Member Cosponsored Legislation](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/MemberEndpoint.md)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bioguideId` | path | `string` | yes | The bioguide identifier for the congressional member. For example, L000174. |
