# Get Package Timeline with SigningHub

Retrieves package timeline details from SigningHub.

## Endpoint

- **Method:** `GET`
- **Path:** `/v4/packages/:packageId/workflow/timeline`
- **Base URL:** `https://api.signinghub.com`
- **Official documentation:** [Get Package Timeline](https://manuals.ascertia.com/SigningHub/10.0/Api/#tag/Document-Package/operation/V4_Package_GetPackageTimeline)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `packageId` | path | `number` | yes | Package ID of the document package. |
