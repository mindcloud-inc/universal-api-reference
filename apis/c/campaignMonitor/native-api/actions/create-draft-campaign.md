# Create Draft Campaign with Campaign Monitor

Creates a draft campaign in Campaign Monitor.

## Endpoint

- **Method:** `POST`
- **Path:** `/campaigns/:clientId.json`
- **Base URL:** `https://api.createsend.com/api/v3.3`
- **Official documentation:** [Create Draft Campaign](https://www.campaignmonitor.com/api/v3-3/campaigns/#creating-draft-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | path | `string` | yes | Campaign Monitor client identifier. |
| `Name` | body | `string` | yes | Internal name of the campaign. |
| `Subject` | body | `string` | yes | Campaign email subject line. |
| `FromName` | body | `string` | yes | Sender name for the campaign. |
| `FromEmail` | body | `string` | yes | Sender email address for the campaign. |
| `ReplyTo` | body | `string` | yes | Reply-to email address for the campaign. |
| `HtmlUrl` | body | `string` | yes | URL of the hosted HTML content for the campaign. |
| `TextUrl` | body | `string` | no | URL of the hosted plain-text content for the campaign. |
| `ListIDs[]` | body | `array<string>` | no | Recipient list identifiers for the campaign. |
| `SegmentIDs[]` | body | `array<string>` | no | Recipient segment identifiers for the campaign. |
| `InlineCSS` | body | `boolean` | no | Whether to inline CSS when creating the campaign. |
