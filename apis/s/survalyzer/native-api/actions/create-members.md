# Create Members with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Panel/v3/CreateMembers`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [Create Members](https://developer.survalyzer.com/knowledge-base/code-examples/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `tenant` | body | `string` | no |
| `panelId` | body | `number` | yes |
| `members[]` | body | `array<object>` | yes |
