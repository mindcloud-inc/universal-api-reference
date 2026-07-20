# Create Draft Campaign with CreateSend

Creates a draft campaign in CreateSend.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:clientId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Create Draft Campaign](https://www.campaignmonitor.com/api/v3-3/campaigns/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `clientId` | path | `string` | yes |
| `Name` | body | `string` | yes |
| `Subject` | body | `string` | yes |
| `FromName` | body | `string` | yes |
| `FromEmail` | body | `string` | yes |
| `ReplyTo` | body | `string` | yes |
| `HtmlUrl` | body | `string` | yes |
| `TextUrl` | body | `string` | no |
| `ListIDs[]` | body | `array<string>` | no |
| `SegmentIDs[]` | body | `array<string>` | no |
| `InlineCSS` | body | `boolean` | no |
