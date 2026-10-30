# Delete Submission with GoCanvas

## Endpoint

- **Method:** `DELETE`
- **Path:** `/submissions/:submissionId`
- **Base URL:** `https://www.gocanvas.com/api/v3`
- **Official documentation:** [Delete Submission](https://api.gocanvas.com/api/v3/docs#delete-a-submission)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `string` | yes | — |
| `hard_delete` | query | `boolean` | no | Permanently deletes the submission when true. Omit for soft delete. |
