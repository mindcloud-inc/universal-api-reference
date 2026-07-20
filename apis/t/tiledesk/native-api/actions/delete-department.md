# Delete Department with Tiledesk

Deletes a department from the current Tiledesk project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/{projectId}/departments/:depId`
- **Base URL:** `https://api.tiledesk.com/v3`
- **Official documentation:** [Delete Department](https://developer.tiledesk.com/apis/rest-api/management-api/departments)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `depId` | path | `string` | yes | The department identifier. |
