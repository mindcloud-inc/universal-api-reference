# Get Team Folders in a Team with Zoho WorkDrive

Retrieves team folders from a Zoho WorkDrive team.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/teams/:teamId/teamfolders`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Get Team Folders in a Team](https://workdrive.zoho.com/apidocs/v1/teams/getteamfoldersinateam)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `teamId` | path | `string` | yes | The WorkDrive team ID. |
| `filter[type]` | query | `string` | no | Filter the team folders by resource type. |
| `page[limit]` | query | `string` | no | Maximum number of records to return. |
| `page[offset]` | query | `string` | no | Number of records to skip before returning results. |
