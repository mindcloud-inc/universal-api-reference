# Trigger Alert with SIGNL4

Creates an alert in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/alerts`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Trigger Alert](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments[]` | body | `array<object>` | no | — |
| `category` | body | `string` | no | — |
| `externalId` | body | `string` | no | — |
| `flags` | body | `number` | no | <p/><ul><li>0 = None</li><li>1 = HasAttachments</li><li>2 = HasAnnotations</li><li>4 = IsBreached</li><li>8 = HasLocationInfo</li><li>16 = EscalatedToTeam</li><li>32 = EscalatedToManager</li><li>64 = CreatedByEscalation</li></ul> |
| `parameters[]` | body | `array<object>` | no | — |
| `severity` | body | `number` | no | <p/><ul><li>0 = Low</li><li>1 = Major</li><li>2 = Critical</li></ul> |
| `teamId` | body | `string` | yes | — |
| `text` | body | `string` | yes | — |
| `title` | body | `string` | yes | — |
