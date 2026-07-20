# List Project Risks with Teamwork Projects

Retrieves project risks from Teamwork Projects.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/{{projectId}}/risks`
- **Base URL:** `{apiEndPoint}projects/api/v3`
- **Official documentation:** [List Project Risks](https://apidocs.teamwork.com/docs/teamwork/v3/risks/get-projects-api-v3-projects-project-id-risks/)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `projectId` | path | `number` | yes | Teamwork project ID. |
