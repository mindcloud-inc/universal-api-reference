# YouGile: List recent tasks

Retrieves recent tasks from YouGile in reverse order.

```
GET https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-recent-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a YouGile `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-recent-tasks?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youGile/latest/actions/list-recent-tasks?${params}`, {
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
| `includeDeleted` | boolean | no | Include deleted tasks in the result. |
| `title` | string | no | Filter tasks by title. |
| `columnId` | string | no | Filter tasks by column ID. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assignedTo` | string | no | Filter tasks by assignee user ID. |
| `stickerId` | string | no | Filter tasks by sticker ID. |
| `stickerStateId` | string | no | Filter tasks by sticker state ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": [
        {}
      ],
      "paging": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | array<object> |  |
| `paging` | object |  |

## Native endpoint

Through the native YouGile API, this operation is `GET /tasks` (base URL `{{credentials.companyDomain}}/api-v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-recent-tasks.md) for the provider-specific parameters and requirements.

