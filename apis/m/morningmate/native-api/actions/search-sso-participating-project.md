# Search SSO Participating Project with Morningmate

Retrieves a Morningmate SSO project for a participant.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/sso/projects/[:projectId]/participants/[:participantId]`
- **Base URL:** `https://api.morningmate.com`
- **Official documentation:** [Search SSO Participating Project](https://api.morningmate.com/docs/api/v1/sso)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectId` | path | `number` | yes |
| `participantId` | path | `string` | yes |
