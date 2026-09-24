# Create Attachment with Sage Intacct

Create a supporting document in a Sage Intacct attachment folder, with optional files encoded as base64.

## Endpoint

- **Method:** `POST`
- **Base URL:** `https://api.intacct.com/ia/xml/xmlgw.phtml`
- **Official documentation:** [Create Attachment](https://developer.intacct.com/api/company-console/attachments/#create-attachment-legacy)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/xml` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments[].attachmentdata` | body | `string` | yes | Base64-encoded binary file content. |
| `supdocid` | body | `string` | no | Required only when attachment autonumbering is not configured in Sage Intacct. |
| `attachments[].attachmenttype` | body | `string` | yes | File extension without a period, for example pdf. |
| `supdocname` | body | `string<object>` | yes | — |
| `attachments[].attachmentname` | body | `string<object>` | yes | File name without the period or extension. |
| `supdocfoldername` | body | `string` | yes | — |
| `supdocdescription` | body | `string` | no | — |
| `locationid` | body | `string` | no | Optional entity location ID for a multi-entity Sage Intacct login. |
| `attachments[]` | body | `array<object>` | no | — |
