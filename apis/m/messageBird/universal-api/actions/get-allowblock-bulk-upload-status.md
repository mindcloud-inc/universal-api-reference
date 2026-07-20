# MessageBird: Get Allow/Block Bulk Upload Status



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-allowblock-bulk-upload-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-allowblock-bulk-upload-status?connectionId=$CONNECTION_ID&workspaceId=string&bulkId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "bulkId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-allowblock-bulk-upload-status?${params}`, {
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
| `workspaceId` | string | yes | The Bird workspace ID that owns the bulk upload. |
| `bulkId` | string | yes | The Bird bulk upload ID to inspect. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bulkId": "string",
      "currentIndex": 1,
      "errors": [
        "string"
      ],
      "status": "string",
      "total": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bulkId` | string |  |
| `currentIndex` | number |  |
| `errors` | array<string> |  |
| `status` | string |  |
| `total` | number |  |
| `updatedAt` | date |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/conversation-allowblock-rules-bulk/:bulkId/status` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-allowblock-bulk-upload-status.md) for the provider-specific parameters and requirements.

