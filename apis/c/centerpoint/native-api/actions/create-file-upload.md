# Create File Upload with Centerpoint

## Endpoint

- **Method:** `POST`
- **Path:** `file/url`
- **Base URL:** `https://api.centerpointconnect.io/centerpoint/`
- **Official documentation:** [Create File Upload](https://api-portal.centerpointconnect.io/portal/catalogue-products/premium-access-product-1/3dea94894ff94ee0588950e6f813f214/docs#/operations/filesPOST)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Original filename sent to Centerpoint. |
| `sourceFile` | body | `file` | yes | File content. The action converts bare base64 to Centerpoint's required data URI format before sending. |
| `subjectType` | body | `list<string>` | yes | Centerpoint subject type for the file attachment. Accepted values: `companies`, `productions`, `properties`. |
| `subjectId` | body | `string` | yes | Centerpoint subject id to attach the uploaded file to. For company attachments, use the Centerpoint company id. |
| `tags[]` | body | `array<string>` | no | Centerpoint model file tags, for example ["Photos"]. |
| `thumbnailSize` | body | `number` | no | Thumbnail size for image uploads. Centerpoint examples use 390. |
| `title` | body | `string` | no | Display title for the Centerpoint file. Maximum length: 255. |
| `description` | body | `string` | no | Optional file description. |
