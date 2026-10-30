# Delete Submission Value with GoCanvas

## Endpoint

- **Method:** `DELETE`
- **Path:** `/submissions/:submissionId/values/:valueId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Delete Submission Value](https://api.gocanvas.com/api/v3/docs#delete-a-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `string` | yes | Numeric ID or mobile GUID of the submission. |
| `valueId` | path | `number` | yes | Identifier of the value to delete. |
