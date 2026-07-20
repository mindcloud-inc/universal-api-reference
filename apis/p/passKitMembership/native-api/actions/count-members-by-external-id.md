# Count Members By External ID with PassKit Membership

Retrieves a member count by external ID in PassKit Membership.

## Endpoint

- **Method:** `POST`
- **Path:** `/members/count/:programId`
- **Base URL:** `https://api.pub2.passkit.io`
- **Official documentation:** [Count Members By External ID](https://help.passkit.com/en/articles/4133757-membership-protocol-filtering-listing-and-counting-by-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `filterGroups[0].fieldFilters[0].filterValue` | body | `string` | yes | Member external id to count by. |
| `programId` | path | `string` | yes | PassKit program id to count within. |
