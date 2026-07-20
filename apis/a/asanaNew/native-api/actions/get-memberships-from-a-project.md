# Get memberships from a project with Asana

Retrieves project memberships from Asana.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:project_gid/project_memberships`
- **Base URL:** `https://app.asana.com/api/1.0`
- **Official documentation:** [Get memberships from a project](https://developers.asana.com/reference/getprojectmembershipsforproject)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `project_gid` | path | `string` | yes | Asana project gid parameter. |
| `user` | query | `string` | no | Asana user parameter. |
| `opt_pretty` | query | `boolean` | no | Asana opt pretty parameter. |
| `limit` | query | `number` | no | Asana limit parameter. |
| `offset` | query | `string` | no | Asana offset parameter. |
| `opt_fields` | query | `list<string>` | no | Asana opt fields parameter. |
