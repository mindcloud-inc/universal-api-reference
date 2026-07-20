# Speak Ai: Get Recorder

Retrieves recorder details from Speak Ai.

```
GET https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-recorder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-recorder?connectionId=$CONNECTION_ID&recorderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "recorderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/get-recorder?${params}`, {
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
| `recorderId` | string | yes | Speak Ai recorder identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "domain": "string",
      "folderId": "string",
      "isActive": true,
      "isAutoAnalyze": true,
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
      "password": "string",
      "privacyMode": "string",
      "recorderId": "string",
      "sourceLanguage": "string",
      "token": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `domain` | string |  |
| `folderId` | string |  |
| `isActive` | boolean |  |
| `isAutoAnalyze` | boolean |  |
| `maxDuration` | number |  |
| `meta.client.email` | boolean |  |
| `meta.client.name` | boolean |  |
| `meta.fontFamily` | string |  |
| `meta.primaryColor` | string |  |
| `meta.type.audio` | boolean |  |
| `meta.type.screenShare` | boolean |  |
| `meta.type.upload.file` | boolean |  |
| `meta.type.upload.multiple` | boolean |  |
| `meta.type.upload.text` | boolean |  |
| `meta.type.upload.url` | boolean |  |
| `meta.type.video` | boolean |  |
| `minDuration` | number |  |
| `name` | string |  |
| `notification.client` | boolean |  |
| `notification.upload` | boolean |  |
| `password` | string |  |
| `privacyMode` | string |  |
| `recorderId` | string |  |
| `sourceLanguage` | string |  |
| `token` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Speak Ai API, this operation is `GET /recorder/:recorderId` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recorder.md) for the provider-specific parameters and requirements.

