# Update Site Membership with Fingertip

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v1/site-memberships/:membershipId`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Update Site Membership](https://docs.fingertip.com/openapi-specs/update-site-membership.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `membershipId` | path | `string` | yes | ID of the site membership to update. |
| `role` | body | `string` | yes | New membership role. |
