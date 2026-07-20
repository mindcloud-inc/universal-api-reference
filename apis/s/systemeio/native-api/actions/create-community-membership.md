# Create Community Membership with Systeme.io

Creates a membership in a Systeme.io community.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/community/communities/:communityId/memberships`
- **Base URL:** `https://api.systeme.io`
- **Official documentation:** [Create Community Membership](https://developer.systeme.io/reference/api_communitycommunities_communityidmemberships_post-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `communityId` | path | `string` | yes | Community identifier. |
| `contactId` | body | `number` | yes | Contact ID to grant community access. |
