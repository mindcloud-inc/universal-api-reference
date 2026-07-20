# Get Async Document Status with DocRaptor

Retrieves async document job status from DocRaptor.

## Endpoint

- **Method:** `GET`
- **Path:** `https://docraptor.com/status/:status_id`
- **Base URL:** `https://api.docraptor.com`
- **Official documentation:** [Get Async Document Status](https://docraptor.com/documentation/api/async)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `status_id` | path | `string` | yes | Status ID returned by a DocRaptor async document creation request. |
