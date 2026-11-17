# Plaud AI: Get Recording



```
GET https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-recording
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Plaud AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-recording?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/plaud/latest/actions/get-recording?${params}`, {
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
| `fileId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "duration": 1,
      "id": "string",
      "name": "Ava Chen",
      "noteList": [
        {
          "dataContent": "string",
          "dataErrorCode": 1,
          "dataId": "string",
          "dataLink": "https://example.com",
          "dataPath": "string",
          "dataTabName": "Ava Chen",
          "dataTitle": "string",
          "dataType": "string"
        }
      ],
      "presignedUrl": "https://example.com",
      "serialNumber": "string",
      "sourceList": [
        {
          "dataContent": "string",
          "dataId": "string",
          "dataLink": "https://example.com",
          "dataTitle": "string",
          "dataType": "string"
        }
      ],
      "startAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `duration` | number |  |
| `id` | string |  |
| `name` | string |  |
| `noteList[].dataContent` | string |  |
| `noteList[].dataErrorCode` | number |  |
| `noteList[].dataId` | string |  |
| `noteList[].dataLink` | string |  |
| `noteList[].dataPath` | string |  |
| `noteList[].dataTabName` | string |  |
| `noteList[].dataTitle` | string |  |
| `noteList[].dataType` | string |  |
| `presignedUrl` | string |  |
| `serialNumber` | string |  |
| `sourceList[].dataContent` | string |  |
| `sourceList[].dataId` | string |  |
| `sourceList[].dataLink` | string |  |
| `sourceList[].dataTitle` | string |  |
| `sourceList[].dataType` | string |  |
| `startAt` | date |  |

## Native endpoint

Through the native Plaud AI API, this operation is `POST /mcp` (base URL `https://mcp.plaud.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-recording.md) for the provider-specific parameters and requirements.

