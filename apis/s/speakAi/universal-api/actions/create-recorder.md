# Speak Ai: Create Recorder

Creates a recorder in Speak Ai.

```
POST https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-recorder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-recorder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/create-recorder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Display name for the recorder. |
| `description` | string | no | Optional description for the recorder. |
| `folderId` | string | no | Optional folder for recordings created by this recorder. |
| `sourceLanguage` | string | no | Optional source language for recorder submissions. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `minDuration` | number | no | Optional minimum recording length in seconds. |
| `maxDuration` | number | no | Optional maximum recording length in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "domain": "string",
      "recorderData": {
        "companyId": "string",
        "createdAt": "2026-05-07T12:00:00.000Z",
        "description": "string",
        "folderId": "string",
        "isActive": true,
        "isAutoAnalyze": true,
        "isDeleted": true,
        "isDisabled": true,
        "maxDuration": 1,
        "meta": {
          "client": {
            "email": true,
            "name": true
          },
          "fontFamily": "string",
          "primaryColor": "string",
          "type": {
            "audio": true,
            "screenShare": true,
            "upload": {
              "file": true,
              "multiple": true,
              "text": true,
              "url": true
            },
            "video": true
          }
        },
        "minDuration": 1,
        "name": "Ava Chen",
        "notification": {
          "client": true,
          "upload": true
        },
        "privacyMode": "string",
        "recorderId": "string",
        "sourceLanguage": "string",
        "token": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "userId": "string"
      },
      "recorderId": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `domain` | string |  |
| `recorderData.companyId` | string |  |
| `recorderData.createdAt` | date |  |
| `recorderData.description` | string |  |
| `recorderData.folderId` | string |  |
| `recorderData.isActive` | boolean |  |
| `recorderData.isAutoAnalyze` | boolean |  |
| `recorderData.isDeleted` | boolean |  |
| `recorderData.isDisabled` | boolean |  |
| `recorderData.maxDuration` | number |  |
| `recorderData.meta.client.email` | boolean |  |
| `recorderData.meta.client.name` | boolean |  |
| `recorderData.meta.fontFamily` | string |  |
| `recorderData.meta.primaryColor` | string |  |
| `recorderData.meta.type.audio` | boolean |  |
| `recorderData.meta.type.screenShare` | boolean |  |
| `recorderData.meta.type.upload.file` | boolean |  |
| `recorderData.meta.type.upload.multiple` | boolean |  |
| `recorderData.meta.type.upload.text` | boolean |  |
| `recorderData.meta.type.upload.url` | boolean |  |
| `recorderData.meta.type.video` | boolean |  |
| `recorderData.minDuration` | number |  |
| `recorderData.name` | string |  |
| `recorderData.notification.client` | boolean |  |
| `recorderData.notification.upload` | boolean |  |
| `recorderData.privacyMode` | string |  |
| `recorderData.recorderId` | string |  |
| `recorderData.sourceLanguage` | string |  |
| `recorderData.token` | string |  |
| `recorderData.updatedAt` | date |  |
| `recorderData.userId` | string |  |
| `recorderId` | string |  |
| `token` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `POST /recorder/create` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-recorder.md) for the provider-specific parameters and requirements.

