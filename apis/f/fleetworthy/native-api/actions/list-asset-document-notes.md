# List Asset Document Notes with Fleetworthy

## Endpoint

- **Method:** `GET`
- **Path:** `/assets/documents/asset-document-notes/from-parent/:parentId`
- **Base URL:** `https://apis.fleetworthy.com/compliance-api/v1`
- **Official documentation:** [List Asset Document Notes](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=get-assets-documents-asset-document-notes-from-parent-parentid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `parentId` | path | `string` | yes | The unique identifier of the note's parent entity. |
| `documentType` | query | `list<string>` | no | The asset document type. Accepted values: `Accident`, `Asset2290`, `MaintenanceEvent`, `MaintenanceInspection`, `MaintenanceRepair`, `Prerequisite`. |
