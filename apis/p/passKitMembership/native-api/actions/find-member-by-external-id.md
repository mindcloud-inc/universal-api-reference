# Find Member By External ID with PassKit Membership

Finds a member in PassKit Membership by external ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/member/list/:programId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Find Member By External ID](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterGroups[0].fieldFilters[0].filterValue` | body | `string` | yes | Member external id to look up. |
| `programId` | path | `string` | yes | PassKit program id to search within. |
