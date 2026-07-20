# Get Department with Tiledesk

Retrieves a department from the current Tiledesk project.

## Endpoint

- **Method:** `GET`
- **Path:** `/{projectId}/departments/:depId`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Get Department](https://developer.tiledesk.com/apis/rest-api/management-api/departments#get-a-department-by-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `depId` | path | `string` | yes | The department identifier. |
