# Start a Feed with Zoho Connect

Creates a new feed in Zoho Connect.

## Endpoint

- **Method:** `POST`
- **Path:** `/pulse/api/v2/addStream`
- **Base URL:** `https://connect.zoho.com`
- **Official documentation:** [Start a Feed](https://www.zoho.com/connect/api/start-a-feed.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `scopeID` | query | `string` | yes | ID of the network where the post should be shared. |
| `partitionID` | query | `string` | no | Optional group or company wall partition ID. |
| `streamContent` | query | `string` | yes | Content for the post. Maximum length is 10000 characters and it supports mentions plus rich formatting. |
| `streamTitle` | query | `string` | no | Optional title for the post. |
| `linkURL` | query | `string` | no | Optional link to attach to the post. |
| `linkDesc` | query | `string` | no | Optional description for the attached link. |
| `linkTitle` | query | `string` | no | Optional title for the attached link. |
| `linkImage` | query | `string` | no | Optional image URL for the attached link. |
| `fileIds` | query | `string` | no | Comma-separated file IDs from the upload Files API. Up to 10 files can be attached. Send multiple values as a string separated by `,`. |
