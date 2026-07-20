# Create Campaign with SendX

## Endpoint

- **Method:** `POST`
- **Path:** `/campaign`
- **Base URL:** `https://api.sendx.io/api/v1/rest`
- **Official documentation:** [Create Campaign](https://docs.sendx.io/api-reference/campaign/create-campaign)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `subject` | body | `string` | yes |
| `sender` | body | `string` | yes |
| `htmlCode` | body | `string` | yes |
| `previewText` | body | `string` | no |
| `plainText` | body | `string` | no |
| `scheduleType` | body | `number` | no |
| `scheduleCondition` | body | `string` | no |
| `timeCondition` | body | `string` | no |
| `timezone` | body | `string` | no |
| `preferredTimezone` | body | `string` | no |
| `preferredTimeCondition` | body | `string` | no |
| `sendInContactsTimezone` | body | `boolean` | no |
| `smartSend` | body | `boolean` | no |
| `includedSegments[]` | body | `array<string>` | no |
| `includedLists[]` | body | `array<string>` | no |
| `includedTags[]` | body | `array<string>` | no |
| `excludedSegments[]` | body | `array<string>` | no |
| `excludedLists[]` | body | `array<string>` | no |
| `excludedTags[]` | body | `array<string>` | no |
