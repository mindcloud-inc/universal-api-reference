# Create Campaign with Reply

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/campaigns`
- **Base URL:** `https://api.reply.io`
- **Official documentation:** [Create Campaign](https://apidocs.reply.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `emailAccounts[]` | body | `array<string>` | yes | Email accounts used to send campaign emails. |
| `name` | body | `string` | yes | Campaign name. |
| `ScheduleId` | body | `number` | no | Optional Reply schedule identifier for the campaign. |
| `settings.DailyThrottling` | body | `number` | yes | Prospects processed in a 24-hour period. |
| `settings.daysToFinishProspect` | body | `number` | yes | Days taken for a prospect to finish the sequence. |
| `settings.disableOpensTracking` | body | `boolean` | yes | Disable email open tracking. |
| `settings.emailsCountPerDay` | body | `number` | yes | Maximum emails sent daily. |
| `settings.EmailSendingDelaySeconds` | body | `number` | yes | Delay between email sends in seconds. |
| `settings.enableLinksTracking` | body | `boolean` | yes | Enable click tracking for links. |
| `settings.RepliesHandlingType` | body | `string` | yes | How Reply handles responses to the campaign. |
| `settings.useDailyThrottling` | body | `boolean` | no | Whether Reply enforces the daily throttling limit. |
| `steps[].InMinutesCount` | body | `number` | yes | Delay in minutes before the step runs. |
| `steps[].number` | body | `number` | yes | Sequence step number. |
| `steps[].templates[].attachmentsIds[]` | body | `array<number>` | no | Attachment identifiers for the template variant. |
| `steps[].templates[].body` | body | `string` | no | Custom body text for the step template variant. |
| `steps[].templates[].CcList` | body | `string` | no | Comma-separated CC recipients for the template variant. |
| `steps[].templates[].emailTemplateId` | body | `number` | no | Existing Reply email template identifier for the variant. |
| `steps[].templates[].subject` | body | `string` | no | Custom subject text for the step template variant. |
| `useDefaultEmailAccountFallback` | body | `boolean` | no | Assign the default email account when no explicit account is provided. |
