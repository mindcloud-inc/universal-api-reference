# Update Team Member with Filestage

Updates a team member in Filestage.

## Endpoint

- **Method:** `PUT`
- **Path:** `/team/members/{memberId}`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Update Team Member](https://developers.filestage.io/docs/api/93vg9wo9b797d-update-team-member)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email |
| `memberId` | path | `string` | yes | Filestage user id |
| `email` | body | `string` | no | — |
