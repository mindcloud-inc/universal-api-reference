# Create Site Membership with Fingertip

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/sites/:siteId/memberships`
- **Base URL:** `https://api.fingertip.com`
- **Official documentation:** [Create Site Membership](https://docs.fingertip.com/openapi-specs/create-site-membership.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `siteId` | path | `string` | yes | Site ID. |
| `userId` | body | `string` | yes | User ID. |
| `role` | body | `string` | yes | Membership role. |
