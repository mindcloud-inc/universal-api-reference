# Delete Members with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Panel/v3/DeleteMembers`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [Delete Members](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `panelId` | body | `number` | yes |
| `panelMembersIds[]` | body | `array<number>` | yes |
| `keepInterviews` | body | `boolean` | no |
