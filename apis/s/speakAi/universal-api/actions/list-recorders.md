# Speak Ai: List Recorders

Retrieves recorders from Speak Ai.

```
GET https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/list-recorders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Speak Ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/list-recorders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/speakAi/latest/actions/list-recorders?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filterName` | string | no | Filter recorders by name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "recorderList": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "folderId": "string",
          "isActive": true,
          "name": "Ava Chen",
          "privacyMode": "string",
          "recorderId": "string",
          "sourceLanguage": "string",
          "token": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ],
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `recorderList[].createdAt` | date |  |
| `recorderList[].description` | string |  |
| `recorderList[].folderId` | string |  |
| `recorderList[].isActive` | boolean |  |
| `recorderList[].name` | string |  |
| `recorderList[].privacyMode` | string |  |
| `recorderList[].recorderId` | string |  |
| `recorderList[].sourceLanguage` | string |  |
| `recorderList[].token` | string |  |
| `recorderList[].updatedAt` | date |  |
| `totalCount` | number |  |

## Native endpoint

Through the native Speak Ai API, this operation is `GET /recorder` (base URL `https://api.speakai.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recorders.md) for the provider-specific parameters and requirements.

