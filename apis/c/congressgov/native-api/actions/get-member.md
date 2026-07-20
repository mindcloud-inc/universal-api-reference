# Get Member with Congress.gov

Retrieves a member from Congress.gov.

## Endpoint

- **Method:** `GET`
- **Path:** `/member/:bioguideId`
- **Base URL:** `https://api.congress.gov/v3`
- **Official documentation:** [Get Member](https://github.com/LibraryOfCongress/api.congress.gov/blob/main/Documentation/MemberEndpoint.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bioguideId` | path | `string` | yes | The bioguide identifier for the congressional member. For example, L000174. |
