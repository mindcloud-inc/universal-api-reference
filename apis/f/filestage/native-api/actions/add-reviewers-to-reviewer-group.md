# Add Reviewers to Reviewer Group with Filestage

Adds reviewers to a Filestage reviewer group.

## Endpoint

- **Method:** `POST`
- **Path:** `/steps/{stepId}/reviewers`
- **Base URL:** `https://api.filestage.io/ext/v2`
- **Official documentation:** [Add Reviewers to Reviewer Group](https://developers.filestage.io/docs/api/9082lw60y3i2v-add-reviewers-to-reviewer-group)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `stepId` | path | `string` | yes | Step Id |
| `reviewerEmails[]` | body | `array<string>` | yes | This is an array of collaborators' emails. This can only contain the emails of existing team members |
| `message` | body | `string` | no | This is a custom message that would be sent to invited reviewers. |
| `notifyEmail` | body | `boolean` | no | When `true` a notification email would be sent to the invited reviewers and when `false` no emails are sent. |
| `requestDecision` | body | `boolean` | no | — |
