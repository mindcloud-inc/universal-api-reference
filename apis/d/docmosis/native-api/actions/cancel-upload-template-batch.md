# Cancel Upload Template Batch with Docmosis

## Endpoint

- **Method:** `POST`
- **Path:** `/uploadTemplateBatchCancel`
- **Base URL:** `{baseUrl}`
- **Official documentation:** [Cancel Upload Template Batch](https://resources.docmosis.com/Documentation/Cloud/DWS4/Cloud-Web-Services-Guide-DWS4.pdf#page=46)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userJobId` | body | `string` | yes | Identifier for the template batch upload job to cancel. |
