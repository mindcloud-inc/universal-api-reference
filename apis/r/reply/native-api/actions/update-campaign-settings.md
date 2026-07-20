# Update Campaign Settings with Reply

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/campaigns/:campaignId`
- **Base URL:** `https://api.reply.io`
- **Official documentation:** [Update Campaign Settings](https://apidocs.reply.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaignId` | path | `number` | yes | Reply campaign identifier. |
| `emailAccounts[]` | body | `array<string>` | no | Email accounts used to send campaign emails. |
| `name` | body | `string` | yes | Campaign name. |
| `settings.dailyThrottling` | body | `number` | yes | Prospects processed in a 24-hour period. |
| `settings.daysToFinishProspect` | body | `number` | yes | Days taken for a prospect to finish the sequence. |
| `settings.disableOpensTracking` | body | `boolean` | yes | Disable email open tracking. |
| `settings.EmailsCountPerDay` | body | `number` | yes | Maximum emails sent daily. |
| `settings.emailSendingDelaySeconds` | body | `number` | yes | Delay between email sends in seconds. |
| `settings.enableLinksTracking` | body | `boolean` | yes | Enable click tracking for links. |
| `settings.repliesHandlingType` | body | `string` | yes | How Reply handles responses to the campaign. |
