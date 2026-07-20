# lemlist: Add Webhook

Creates a new webhook in lemlist.

```
POST https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/add-webhook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a lemlist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/add-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://webhook.site/1d50ac35-2755-42cc-964c-9acbb4ebca30"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/add-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://webhook.site/1d50ac35-2755-42cc-964c-9acbb4ebca30"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `targetUrl` | string | yes | The URL that will receive webhook POST requests. Example: `https://webhook.site/1d50ac35-2755-42cc-964c-9acbb4ebca30`. |
| `type` | list<string> | no | Optional event type to subscribe to. One of: `aircallCreated`, `aircallDone`, `aircallEnded`, `aircallInterested`, `aircallNotInterested`, `annotated`, `apiDone`, `apiFailed`, `apiInterested`, `apiNotInterested`, `attracted`, `callRecordingDone`, `callTranscriptDone`, `campaignComplete`, `connectionIssue`, `contacted`, `customDomainErrors`, `emailsBounced`, `emailsClicked`, `emailsFailed`, `emailsInterested`, `emailsNotInterested`, `emailsOpened`, `emailsReplied`, `emailsSendFailed`, `emailsSent`, `emailsUnsubscribed`, `enrichmentDone`, `enrichmentError`, `hooked`, `interested`, `lemwarmPaused`, `linkedinInterested`, `linkedinInviteAccepted`, `linkedinInviteDone`, `linkedinInviteFailed`, `linkedinNotInterested`, `linkedinReplied`, `linkedinSendFailed`, `linkedinSent`, `linkedinVisitDone`, `linkedinVisitFailed`, `linkedinVoiceNoteDone`, `linkedinVoiceNoteFailed`, `manualInterested`, `manualNotInterested`, `notInterested`, `opportunitiesDone`, `paused`, `resumed`, `sendLimitReached`, `skipped`, `warmed`. |
| `campaignId` | string | no | Webhook for a specific campaign. Example: `cam_A1B2C3D4E5F6G7H8I9`. |
| `isFirst` | boolean | no | Webhook for first activity only. |
| `zapId` | string | no | Zapier ID. Example: `123456789`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "id": "string",
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `id` | string |  |
| `targetUrl` | string |  |

## Native endpoint

Through the native lemlist API, this operation is `POST /hooks` (base URL `https://api.lemlist.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-webhook.md) for the provider-specific parameters and requirements.

