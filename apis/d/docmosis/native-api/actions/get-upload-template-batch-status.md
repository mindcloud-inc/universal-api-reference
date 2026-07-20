# Get Upload Template Batch Status with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/uploadTemplateBatchStatus`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Get Upload Template Batch Status](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=44)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userJobId` | body | `string` | yes | Batch upload job identifier returned by Upload Template Batch. |
