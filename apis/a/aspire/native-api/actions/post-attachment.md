# Post Attachment with Aspire

## Endpoint

- **Method:** `POST`
- **Path:** `/Attachments`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [Post Attachment](https://guide.youraspire.com/apidocs/attachments-2)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json;odata.metadata=minimal;odata.streaming=true, application/json;odata.metadata=minimal;odata.streaming=false, application/json;odata.metadata=minimal, application/json;odata.metadata=full;odata.streaming=true, application/json;odata.metadata=full;odata.streaming=false, application/json;odata.metadata=full, application/json;odata.metadata=none;odata.streaming=true, application/json;odata.metadata=none;odata.streaming=false, application/json;odata.metadata=none, application/json;odata.streaming=true, application/json;odata.streaming=false, application/json, application/xml, application/prs.odatatestxx-odata, text/plain, text/json` |

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$filter` | query | `string` | no |
| `AttachmentTypeId` | body | `list<number>` | no |
| `FileName` | body | `string` | no |
| `FileData` | body | `file` | no |
| `ObjectCode` | body | `list<string>` | no |
| `ObjectId` | body | `number` | no |
| `AttachToInvoice` | body | `boolean` | no |
| `ExposeToCrew` | body | `boolean` | no |
