# Upload Person File with Fleetworthy

## Endpoint

- **Method:** `POST`
- **Path:** `/people/files`
- **Base URL:** `https://apis.fleetworthy.com/compliance-api/v1`
- **Official documentation:** [Upload Person File](https://developer.fleetworthy.com/api-details#api=prod-compliance-v1&operation=post-people-files)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `LocationId` | body | `string` | yes | The Fleetworthy location UUID. |
| `ObjectId` | body | `string` | yes | The existing regulated document UUID that will own the file. |
| `ParentObjectId` | body | `string` | yes | The Fleetworthy person UUID that owns the document. |
| `ObjectDisplayName` | body | `string` | yes | The display name for the uploaded report. |
| `SetAsPrimary` | body | `boolean` | yes | Whether the uploaded file is the primary file for the document. |
| `UserId` | body | `string` | no | Optional Fleetworthy user UUID associated with the upload. |
| `MetaData` | body | `string` | yes | Fleetworthy metadata string for the uploaded file. |
| `file` | body | `file` | yes | The file to upload, up to 50 MB. |
