# Create Campaign with Smoove

Creates a new email campaign in Smoove.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/Campaigns`
- **Base URL:** `https://rest.smoove.io`
- **Official documentation:** [Create Campaign](https://rest.smoove.io)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `subject` | body | `string` | no | — |
| `body` | body | `string` | no | — |
| `toMembersByEmail[]` | body | `array<string>` | no | — |
| `toMembersByExternalId[]` | body | `array<string>` | no | — |
| `toMembersById[]` | body | `array<number>` | no | — |
| `toListsById[]` | body | `array<number>` | no | — |
| `excludeFromMembers[]` | body | `array<number>` | no | — |
| `excludeFromLists[]` | body | `array<number>` | no | — |
| `trackLinks` | body | `boolean` | no | — |
| `customUnsubscribeMode` | body | `list` | no | Accepted values: `None`, `PingAndUnsubscribe`, `PingOnly`, `RedirectAndUnsubscribe`, `RedirectOnly`. |
| `externalUnsubscribeUrl` | body | `string` | no | — |
| `customData[]` | body | `array<object>` | no | — |
| `campaignAttachments[]` | body | `array<string>` | no | — |
| `externalId` | body | `string` | no | — |
| `customFromAddress` | body | `string` | no | — |
| `customReplyToAddress` | body | `string` | no | — |
| `sendNow` | query | `boolean` | no | — |
| `scheduleTo` | query | `string` | no | — |
| `templateName` | query | `string` | no | — |
