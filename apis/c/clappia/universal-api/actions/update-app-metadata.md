# Clappia: Update App Metadata

Updates existing app metadata in Clappia.

```
PUT https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-app-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clappia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-app-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "appId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clappia/latest/actions/update-app-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "appId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appId` | string | yes | Clappia app ID. |
| `appName` | string | no | Updated app name. |
| `appDescription` | string | no | Updated app description. |
| `isAnalyticsEnabled` | boolean | no | Whether app analytics should be enabled. |
| `requiresAuthentication` | boolean | no | Whether end users must authenticate to open the app. |
| `allowEmbedding` | boolean | no | Whether the app can be embedded. |
| `requireAuthForSubmissions` | boolean | no | Whether submission access requires authentication. |
| `canUserSubmit` | boolean | no | Whether end users can submit the app. |
| `canUserSaveDraft` | boolean | no | Whether end users can save drafts. |
| `defaultStatus` | string | no | Default status name for new submissions. |
| `postSubmissionMessageText` | string | no | Message shown after a successful submission. |
| `submitButtonLabel` | string | no | Custom label for the submit button. |
| `submissionDisplayName` | string | no | Display name used for submissions. |
| `allowViewingSubmissions` | boolean | no | Whether users can view submissions. |
| `allowSubmitAnother` | boolean | no | Whether users can submit another entry after success. |
| `allowPrintingSubmissions` | boolean | no | Whether users can print submissions. |
| `saveDraftButtonLabel` | string | no | Custom label for the save draft button. |
| `discardDraftButtonLabel` | string | no | Custom label for the discard draft button. |
| `printSubmissionButtonLabel` | string | no | Custom label for the print submission button. |
| `viewSubmissionsButtonLabel` | string | no | Custom label for the view submissions button. |
| `submitAnotherButtonLabel` | string | no | Custom label for the submit another button. |
| `submissionViewMode` | string | no | Submission view mode, such as modal. |
| `defaultAppView` | string | no | Default app view, such as appHome. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statuses[]` | array<object> | no | Array of status configuration objects. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Clappia API returns.

## Native endpoint

Through the native Clappia API, this operation is `POST /appdefinitionv2/updateAppMetadata` (base URL `https://api-public-v4.clappia.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-app-metadata.md) for the provider-specific parameters and requirements.

