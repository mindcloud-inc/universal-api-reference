# Moderation API: Get Queue Items

Retrieves review queue items from Moderation API.

```
GET https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-queue-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moderation API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-queue-items?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moderationAPI/latest/actions/get-queue-items?${params}`, {
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
| `id` | string | yes | The queue ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageSize` | number | no | Number of items per page |
| `pageNumber` | number | no | Page number to fetch |
| `sortField` | string | no |  |
| `sortDirection` | string | no | Sort direction |
| `conversationIds` | string | no |  |
| `labels` | string | no |  |
| `afterDate` | string | no |  |
| `beforeDate` | string | no |  |
| `includeResolved` | string | no |  |
| `authorId` | string | no |  |
| `filteredActionIds` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `pagination` | object |  |

## Native endpoint

Through the native Moderation API API, this operation is `GET /queue/:id/items` (base URL `https://api.moderationapi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-queue-items.md) for the provider-specific parameters and requirements.

