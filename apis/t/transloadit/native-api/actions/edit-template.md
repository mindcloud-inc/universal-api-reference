# Edit Template with Transloadit

Updates an existing template in Transloadit.

## Endpoint

- **Method:** `PUT`
- **Path:** `/templates/:templateId`
- **Base URL:** `https://api2.transloadit.com`
- **Official documentation:** [Edit Template](https://transloadit.com/docs/api/templates-template-id-put/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `templateId` | path | `string` | yes | The ID of the template to edit. |
| `params` | body | `string` | yes | JSON string containing the updated Transloadit template definition. |
