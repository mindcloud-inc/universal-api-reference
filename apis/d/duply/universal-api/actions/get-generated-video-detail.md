# Duply: Get Generated Video Detail

Retrieves details for a generated video from Duply.

```
GET https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-generated-video-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Duply `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-generated-video-detail?connectionId=$CONNECTION_ID&generateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "generateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/duply/latest/actions/get-generated-video-detail?${params}`, {
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
| `generateId` | string | yes | The generated video ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "generatedIdOld": "string",
      "generateFormatId": 1,
      "generateTypeId": 1,
      "id": "string",
      "note": {},
      "progress": "string",
      "requestName": "Ava Chen",
      "source": "string",
      "status": {},
      "templateId": "string",
      "total": {},
      "type": {},
      "updated": "2026-05-07T12:00:00.000Z",
      "userApiId": "string",
      "userId": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date |  |
| `generatedIdOld` | string |  |
| `generateFormatId` | number |  |
| `generateTypeId` | number |  |
| `id` | string |  |
| `note` | object |  |
| `progress` | string |  |
| `requestName` | string |  |
| `source` | string |  |
| `status` | object |  |
| `templateId` | string |  |
| `total` | object |  |
| `type` | object |  |
| `updated` | date |  |
| `userApiId` | string |  |
| `userId` | object |  |

## Native endpoint

Through the native Duply API, this operation is `GET /generate-video/:generateId` (base URL `https://gen.duply.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-generated-video-detail.md) for the provider-specific parameters and requirements.

