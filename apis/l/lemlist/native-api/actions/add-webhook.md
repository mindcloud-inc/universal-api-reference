# Add Webhook with lemlist

Creates a new webhook in lemlist.

## Endpoint

- **Method:** `POST`
- **Path:** `/hooks`
- **Base URL:** `https://api.lemlist.com/api`
- **Official documentation:** [Add Webhook](https://developer.lemlist.com/api-reference/endpoints/webhooks/add-webhook)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `targetUrl` | body | `string` | yes | The URL that will receive webhook POST requests. |
| `type` | body | `list<string>` | no | Optional event type to subscribe to. Accepted values: `aircallCreated`, `aircallDone`, `aircallEnded`, `aircallInterested`, `aircallNotInterested`, `annotated`, `apiDone`, `apiFailed`, `apiInterested`, `apiNotInterested`, `attracted`, `callRecordingDone`, `callTranscriptDone`, `campaignComplete`, `connectionIssue`, `contacted`, `customDomainErrors`, `emailsBounced`, `emailsClicked`, `emailsFailed`, `emailsInterested`, `emailsNotInterested`, `emailsOpened`, `emailsReplied`, `emailsSendFailed`, `emailsSent`, `emailsUnsubscribed`, `enrichmentDone`, `enrichmentError`, `hooked`, `interested`, `lemwarmPaused`, `linkedinInterested`, `linkedinInviteAccepted`, `linkedinInviteDone`, `linkedinInviteFailed`, `linkedinNotInterested`, `linkedinReplied`, `linkedinSendFailed`, `linkedinSent`, `linkedinVisitDone`, `linkedinVisitFailed`, `linkedinVoiceNoteDone`, `linkedinVoiceNoteFailed`, `manualInterested`, `manualNotInterested`, `notInterested`, `opportunitiesDone`, `paused`, `resumed`, `sendLimitReached`, `skipped`, `warmed`. |
| `campaignId` | query | `string` | no | Webhook for a specific campaign. |
| `isFirst` | query | `boolean` | no | Webhook for first activity only. |
| `zapId` | query | `string` | no | Zapier ID. |
