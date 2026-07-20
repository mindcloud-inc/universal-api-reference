# Invite Members with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Distribute/v3/InviteMembers`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [Invite Members](https://developer.survalyzer.com/knowledge-base/code-examples/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `surveyId` | body | `number` | yes |
| `panelId` | body | `number` | yes |
| `samplingProjectId` | body | `number` | no |
| `messageTemplateId` | body | `number` | yes |
| `textBlocks[]` | body | `array<object>` | no |
| `scheduleDateTime` | body | `string` | no |
| `conditions[]` | body | `array<object>` | no |
| `channel` | body | `string` | yes |
| `asyncProcess` | body | `boolean` | no |
| `interviewExpiryDate` | body | `string` | no |
| `from` | body | `string` | no |
| `fromName` | body | `string` | no |
| `replyTo` | body | `string` | no |
| `replyToName` | body | `string` | no |
| `memberIds[]` | body | `array<number>` | no |
