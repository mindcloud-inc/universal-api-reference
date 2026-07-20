# Zoho Webinar: List Recordings

Retrieves recordings from Zoho Webinar by session type.

```
GET https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/list-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Webinar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/list-recordings?connectionId=$CONNECTION_ID&organizationId=%7B%7Bcredentials.organizationId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "{{credentials.organizationId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoWebinar/latest/actions/list-recordings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `organizationId` | string | yes | Default: `{{credentials.organizationId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dateTime": "string",
      "departmentId": 1,
      "departmentName": "Ava Chen",
      "downloadAccess": 1,
      "downloadUrl": "https://example.com",
      "duration": 1,
      "durationInMins": 1,
      "erecordingId": "string",
      "eventTime": "string",
      "fileSize": "string",
      "generateSummaryAllowed": true,
      "id": "string",
      "isGenerating": true,
      "isOpenAIEnabled": true,
      "isSummaryGenerated": true,
      "isTranscriptGenerated": true,
      "isTranscriptionEnabled": true,
      "isWebinar": true,
      "noAudioRecording": true,
      "openAIStatus": "string",
      "playUrl": "https://example.com",
      "recordingId": "string",
      "resourceName": "Ava Chen",
      "sDate": "string",
      "sePresence": true,
      "shareOption": 1,
      "shareUrl": "https://example.com",
      "short_webinar_key": "string",
      "startTimeinMs": 1,
      "status": "string",
      "sTime": "string",
      "summaryAccess": 1,
      "topic": "string",
      "transcriptAccess": 1,
      "webinarKey": "string",
      "zfs_mapping_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dateTime` | string |  |
| `departmentId` | number |  |
| `departmentName` | string |  |
| `downloadAccess` | number |  |
| `downloadUrl` | string |  |
| `duration` | number |  |
| `durationInMins` | number |  |
| `erecordingId` | string |  |
| `eventTime` | string |  |
| `fileSize` | string |  |
| `generateSummaryAllowed` | boolean |  |
| `id` | string |  |
| `isGenerating` | boolean |  |
| `isOpenAIEnabled` | boolean |  |
| `isSummaryGenerated` | boolean |  |
| `isTranscriptGenerated` | boolean |  |
| `isTranscriptionEnabled` | boolean |  |
| `isWebinar` | boolean |  |
| `noAudioRecording` | boolean |  |
| `openAIStatus` | string |  |
| `playUrl` | string |  |
| `recordingId` | string |  |
| `resourceName` | string |  |
| `sDate` | string |  |
| `sePresence` | boolean |  |
| `shareOption` | number |  |
| `shareUrl` | string |  |
| `short_webinar_key` | string |  |
| `startTimeinMs` | number |  |
| `status` | string |  |
| `sTime` | string |  |
| `summaryAccess` | number |  |
| `topic` | string |  |
| `transcriptAccess` | number |  |
| `webinarKey` | string |  |
| `zfs_mapping_id` | string |  |

## Native endpoint

Through the native Zoho Webinar API, this operation is `GET /api/v2/:organizationId/recordings.json` (base URL `https://webinar.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recordings.md) for the provider-specific parameters and requirements.

