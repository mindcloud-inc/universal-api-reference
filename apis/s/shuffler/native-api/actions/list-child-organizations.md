# List Child Organizations with Shuffler

Retrieves child organizations from Shuffler.

## Endpoint

- **Method:** `GET`
- **Path:** `/orgs/{parentOrgId}/suborgs`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [List Child Organizations](https://shuffler.io/docs/API#list-child-organizations)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `cursor` | query | `string` | no | Optional pagination cursor. |
| `parentOrgId` | path | `string` | yes | Parent Org Id path parameter. |
