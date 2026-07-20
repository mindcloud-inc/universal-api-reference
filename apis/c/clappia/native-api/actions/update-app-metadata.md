# Update App Metadata with Clappia

Updates existing app metadata in Clappia.

## Endpoint

- **Method:** `POST`
- **Path:** `/appdefinitionv2/updateAppMetadata`
- **Base URL:** `https://api-public-v4.clappia.com`
- **Official documentation:** [Update App Metadata](https://developer.clappia.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `appId` | body | `string` | yes | Clappia app ID. |
| `appName` | body | `string` | no | Updated app name. |
| `appDescription` | body | `string` | no | Updated app description. |
| `isAnalyticsEnabled` | body | `boolean` | no | Whether app analytics should be enabled. |
| `requiresAuthentication` | body | `boolean` | no | Whether end users must authenticate to open the app. |
| `allowEmbedding` | body | `boolean` | no | Whether the app can be embedded. |
| `requireAuthForSubmissions` | body | `boolean` | no | Whether submission access requires authentication. |
| `canUserSubmit` | body | `boolean` | no | Whether end users can submit the app. |
| `canUserSaveDraft` | body | `boolean` | no | Whether end users can save drafts. |
| `statuses[]` | body | `array<object>` | no | Array of status configuration objects. |
| `defaultStatus` | body | `string` | no | Default status name for new submissions. |
| `postSubmissionMessageText` | body | `string` | no | Message shown after a successful submission. |
| `submitButtonLabel` | body | `string` | no | Custom label for the submit button. |
| `submissionDisplayName` | body | `string` | no | Display name used for submissions. |
| `allowViewingSubmissions` | body | `boolean` | no | Whether users can view submissions. |
| `allowSubmitAnother` | body | `boolean` | no | Whether users can submit another entry after success. |
| `allowPrintingSubmissions` | body | `boolean` | no | Whether users can print submissions. |
| `saveDraftButtonLabel` | body | `string` | no | Custom label for the save draft button. |
| `discardDraftButtonLabel` | body | `string` | no | Custom label for the discard draft button. |
| `printSubmissionButtonLabel` | body | `string` | no | Custom label for the print submission button. |
| `viewSubmissionsButtonLabel` | body | `string` | no | Custom label for the view submissions button. |
| `submitAnotherButtonLabel` | body | `string` | no | Custom label for the submit another button. |
| `submissionViewMode` | body | `string` | no | Submission view mode, such as modal. |
| `defaultAppView` | body | `string` | no | Default app view, such as appHome. |
