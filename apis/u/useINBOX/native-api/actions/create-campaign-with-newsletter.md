# Create Campaign With Newsletter with UseINBOX

Creates a campaign from a newsletter in UseINBOX.

## Endpoint

- **Method:** `POST`
- **Path:** `/inbox/v1/campaigns`
- **Base URL:** `https://useapi.useinbox.com`
- **Official documentation:** [Create Campaign With Newsletter](https://reference.useinbox.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `newsletterId` | body | `string` | yes | Newsletter ID to send as a campaign. |
| `senderAccountId` | body | `string` | yes | Sender account ID used for the campaign. |
| `listType` | body | `number` | yes | INBOX list type value for the campaign audience. |
| `lists[]` | body | `array<string>` | yes | Contact list IDs that should receive the campaign. Send multiple values as a array. |
| `plannedTime` | body | `date` | yes | Scheduled campaign send time. |
| `notifyWhenStart` | body | `boolean` | no | Whether INBOX should notify when the campaign starts. |
| `notifyWhenEnd` | body | `boolean` | no | Whether INBOX should notify when the campaign ends. |
