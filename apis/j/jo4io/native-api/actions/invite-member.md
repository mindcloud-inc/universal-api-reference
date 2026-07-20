# Invite Member with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/teams/:teamSlug/invitations`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Invite Member](https://jo4-api.jo4.io/swagger-ui/index.html#/team-controller/inviteMember)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | yes |
| `role` | body | `string` | no |
| `teamSlug` | path | `string` | yes |
