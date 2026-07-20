# Get Attachment File Data with Aspire

Retrieve a list of information related to an attached file, including the File Data encoded as a base 64 string.

## Endpoint

- **Method:** `GET`
- **Path:** `Attachments/AttachmentFileData`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Get Attachment File Data](https://guide.youraspire.com/apidocs/attachmentsattachmentfiledata-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | yes | This argument requires this filter(without quotes): "AttachmentID eq ID" where ID is the number of the attachment |
