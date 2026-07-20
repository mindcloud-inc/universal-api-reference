# Send Campaign From Draft with GMass

Creates and sends a GMass campaign from a draft.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:campaignDraftId`
- **Base URL:** `https://api.gmass.co/api`
- **Official documentation:** [Send Campaign From Draft](https://api.gmass.co/docs#tag/Campaigns)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `campaignDraftId` | path | `string` | yes |
| `createDrafts` | body | `boolean` | no |
| `friendlyName` | body | `string` | no |
| `openTracking` | body | `boolean` | no |
| `clickTracking` | body | `boolean` | no |
| `sendTime` | body | `string` | no |
| `previewText` | body | `string` | no |
| `replyTo` | body | `string` | no |
| `fromName` | body | `string` | no |
| `verify` | body | `boolean` | no |
