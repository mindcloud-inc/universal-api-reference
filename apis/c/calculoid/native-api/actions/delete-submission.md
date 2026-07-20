# Delete Submission with Calculoid

## Endpoint

- **Method:** `POST`
- **Path:** `/submission/delete/:submissionId`
- **Base URL:** `https://api.calculoid.com`
- **Official documentation:** [Delete Submission](https://www.calculoid.com/documentation-new)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `submissionId` | path | `string` | yes | Calculoid submission ID to delete. |
