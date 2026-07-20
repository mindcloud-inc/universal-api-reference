# Invite Team Member with Filestage

Creates a new team member invitation in Filestage.

## Endpoint

- **Method:** `POST`
- **Path:** `/team/members`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Invite Team Member](https://developers.filestage.io/docs/api/5v0lokos961fz-invite-team-member)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `roleId` | body | `string` | yes |
