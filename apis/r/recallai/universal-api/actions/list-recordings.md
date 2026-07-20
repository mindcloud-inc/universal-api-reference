# Recallai: List Recordings

Retrieves recordings from Recallai.

```
GET https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-recordings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recallai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-recordings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recallai/latest/actions/list-recordings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "bot": "string",
      "completedAt": "string",
      "createdAt": "string",
      "desktopSdkUpload": {},
      "expiresAt": "string",
      "id": "string",
      "mediaShortcuts": {},
      "metadata": {},
      "realtimeEndpoints": [
        "string"
      ],
      "startedAt": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bot` | string |  |
| `completedAt` | string |  |
| `createdAt` | string |  |
| `desktopSdkUpload` | object |  |
| `expiresAt` | string |  |
| `id` | string |  |
| `mediaShortcuts` | object |  |
| `metadata` | object |  |
| `realtimeEndpoints` | array |  |
| `startedAt` | string |  |
| `status` | object |  |

## Native endpoint

Through the native Recallai API, this operation is `GET /api/v1/recording/` (base URL `https://{{credentials.workspaceRegion}}.recall.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-recordings.md) for the provider-specific parameters and requirements.

