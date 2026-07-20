# Create Event Source with SIGNL4

Creates an event source in SIGNL4.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/eventsources`
- **Base URL:** `https://connect.signl4.com/api`
- **Official documentation:** [Create Event Source](https://connect.signl4.com/api/docs/index.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `number` | no | <p/><ul><li>0 = None</li><li>1 = Email</li><li>2 = Webhook</li></ul> |
| `name` | body | `string` | no | — |
| `description` | body | `string` | no | — |
| `teamId` | body | `string` | no | — |
| `disabled` | body | `boolean` | no | — |
| `language` | body | `number` | no | <p/><ul><li>0 = EN</li><li>1 = DE</li></ul> |
| `subType` | body | `string` | no | — |
| `targets[]` | body | `array<object>` | no | — |
| `options` | body | `number` | no | <p/><ul><li>0 = None</li><li>1 = DisableContentParsing</li></ul> |
