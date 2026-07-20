# Send Fax with Documo

Creates a new fax message in Documo.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/faxes`
- **Base URL:** `https://api.documo.com`
- **Official documentation:** [Send Fax](https://docs.documo.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `multipart/form-data` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `faxNumber` | body | `string` | yes | String \| Required \| Destination phone number |
| `coverPage` | body | `boolean` | no | Boolean \| Include system cover page; removes file requirement when true |
| `coverPageId` | body | `string` | no | UUID \| Cover page UUID to include |
| `tags` | body | `string` | no | String \| Comma separated list of tag IDs |
| `recipientName` | body | `string` | no | String \| 40 character limit |
| `senderName` | body | `string` | no | String \| 40 character limit |
| `subject` | body | `string` | no | String \| 55 character limit |
| `callerId` | body | `string` | no | String \| 10 character limit \| Phone number |
| `notes` | body | `string` | no | String \| 4000 character limit |
| `cf` | body | `string` | no | String \| JSON object with custom fields |
| `scheduledDate` | body | `string` | no | String \| ISO date-time for scheduled send |
| `attachments` | body | `file` | no | File \| Required if coverPage is not added |
| `attachmentUrls` | body | `string` | no | String \| URL list for attached documents |
| `fileIds` | body | `string` | no | String \| UUID list of mDrive file entities |
| `async` | body | `boolean` | no | Boolean \| When true, immediately returns only messageId |
| `optimizeFax` | body | `string` | no | String \| auto, text, or image |
