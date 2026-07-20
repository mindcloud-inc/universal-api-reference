# Create Team with jo4.io

## Endpoint

- **Method:** `POST`
- **Path:** `/protected/teams`
- **Base URL:** `https://jo4-api.jo4.io/api/v1`
- **Official documentation:** [Create Team](https://jo4-api.jo4.io/swagger-ui/index.html#/team-controller/createTeam)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `description` | body | `string` | no |
| `logoUrl` | body | `string` | no |
| `name` | body | `string` | yes |
| `teamSlug` | body | `string` | yes |
