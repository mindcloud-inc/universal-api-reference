# Get Uploaded Checklist Files with CheckFlow

## Endpoint

- **Method:** `GET`
- **Path:** `/api/checklist/uploaded-files`
- **Base URL:** `https://app.checkflow.io`
- **Official documentation:** [Get Uploaded Checklist Files](https://docs.checkflow.io/docs/api/checklists#get-uploaded-files)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskContentKey` | query | `string` | yes | The key of the file upload task content control. |
