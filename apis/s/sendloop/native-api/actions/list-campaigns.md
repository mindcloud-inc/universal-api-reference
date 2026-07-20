# List Campaigns with Sendloop

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign.getlist/json`
- **Base URL:** `https://{subdomain}.sendloop.com/api/v3`
- **Official documentation:** [List Campaigns](https://chmyos.notion.site/Get-Campaign-List-555b08159aa64d8cb16ff9e9eb5985a8)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `IgnoreDrafts` | body | `number` | no | Set to 1 to exclude draft campaigns |
| `IgnoreSending` | body | `number` | no | Set to 1 to exclude currently sending campaigns |
| `IgnorePaused` | body | `number` | no | Set to 1 to exclude paused campaigns |
| `IgnoreSent` | body | `number` | no | Set to 1 to exclude sent campaigns |
| `IgnoreFailed` | body | `number` | no | Set to 1 to exclude failed campaigns |
| `IgnoreApproval` | body | `number` | no | Set to 1 to exclude approval-pending campaigns |
