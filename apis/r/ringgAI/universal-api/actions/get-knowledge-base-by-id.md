# Ringg AI: Get Knowledge Base by ID

Retrieves a knowledge base from Ringg AI by ID.

```
GET https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-knowledge-base-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-knowledge-base-by-id?connectionId=$CONNECTION_ID&kbId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "kbId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/get-knowledge-base-by-id?${params}`, {
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
| `kbId` | string | yes | (Required) ID of the knowledge base |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "faqs": [
        {
          "content": {},
          "fileId": "string",
          "fileSize": 1,
          "fileType": "string"
        }
      ],
      "files": [
        {
          "fileId": "string",
          "filename": "Ava Chen",
          "filePath": "string",
          "fileSize": 1,
          "fileType": "string"
        }
      ],
      "kbId": "string",
      "kbName": "Ava Chen",
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urls": [
        {
          "fileId": "https://example.com",
          "filePath": "https://example.com",
          "fileSize": 1,
          "fileType": "https://example.com",
          "url": "https://example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `faqs` | array<object> |  |
| `faqs[].content` | object |  |
| `faqs[].fileId` | string |  |
| `faqs[].fileSize` | number |  |
| `faqs[].fileType` | string |  |
| `files` | array<object> |  |
| `files[].fileId` | string |  |
| `files[].filename` | string |  |
| `files[].filePath` | string |  |
| `files[].fileSize` | number |  |
| `files[].fileType` | string |  |
| `kbId` | string |  |
| `kbName` | string |  |
| `status` | string | Processing status of the knowledge base |
| `updatedAt` | date |  |
| `urls` | array<object> |  |
| `urls[].fileId` | string |  |
| `urls[].filePath` | string |  |
| `urls[].fileSize` | number |  |
| `urls[].fileType` | string |  |
| `urls[].url` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `GET /external/kb/:kb_id` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-knowledge-base-by-id.md) for the provider-specific parameters and requirements.

