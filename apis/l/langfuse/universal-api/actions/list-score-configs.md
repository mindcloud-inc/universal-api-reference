# Langfuse: List Score Configs

Retrieves score configs from Langfuse.

```
GET https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-score-configs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Langfuse `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-score-configs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-score-configs?${params}`, {
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
      "categories": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dataType": "string",
      "description": "string",
      "id": "string",
      "isArchived": true,
      "maxValue": 1,
      "minValue": 1,
      "name": "Ava Chen",
      "projectId": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories` | array<object> |  |
| `createdAt` | date |  |
| `dataType` | string |  |
| `description` | string |  |
| `id` | string |  |
| `isArchived` | boolean |  |
| `maxValue` | number |  |
| `minValue` | number |  |
| `name` | string |  |
| `projectId` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Langfuse API, this operation is `GET /score-configs` (base URL `https://cloud.langfuse.com/api/public`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-score-configs.md) for the provider-specific parameters and requirements.

