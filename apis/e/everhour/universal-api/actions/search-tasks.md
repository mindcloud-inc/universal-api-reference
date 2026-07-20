# Everhour: Search Tasks

Finds tasks in Everhour by search query.

```
GET https://connect.mindcloud.co/v1/universal/everhour/latest/actions/search-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everhour `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/everhour/latest/actions/search-tasks?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/everhour/latest/actions/search-tasks?${params}`, {
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
| `limit` | number | no | Maximum number of records to return. |
| `query` | string | no | Task search query. |
| `searchInClosed` | boolean | no | Include closed tasks in the search results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_type": "string",
      "assignees": [
        {}
      ],
      "completed": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": 1,
      "id": "string",
      "labels": [
        {}
      ],
      "name": "Ava Chen",
      "position": 1,
      "projects": [
        "string"
      ],
      "section": 1,
      "status": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_type` | string |  |
| `assignees` | array<object> |  |
| `completed` | boolean |  |
| `createdAt` | date |  |
| `createdBy` | number |  |
| `id` | string |  |
| `labels` | array<object> |  |
| `name` | string |  |
| `position` | number |  |
| `projects` | array<string> |  |
| `section` | number |  |
| `status` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Everhour API, this operation is `GET /tasks/search` (base URL `https://api.everhour.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tasks.md) for the provider-specific parameters and requirements.

