# Update Mailbox with DitLead

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/mailbox/{mailboxId}`
- **Base URL:** `https://api.ditlead.com`
- **Official documentation:** [Update Mailbox](https://ditlead.com/developer/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignSetting.sendingLimit` | body | `number` | no | — |
| `firstName` | body | `string` | no | — |
| `lastName` | body | `string` | no | — |
| `mailboxId` | path | `string` | yes | Public ID of the mailbox. |
| `warmingSetting.increasePerDay` | body | `number` | no | — |
| `warmingSetting.maximumSendPerDay` | body | `number` | no | — |
| `warmingSetting.randomizeMax` | body | `boolean` | no | — |
| `warmingSetting.replyRate` | body | `number` | no | — |
