# Freshsales Classic: List All Tasks

Retrieves tasks from Freshsales Classic.

```
GET https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshsales Classic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-tasks?connectionId=$CONNECTION_ID&filter=open" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "open"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshsalesClassic/latest/actions/list-all-tasks?${params}`, {
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
| `filter` | string | yes | Freshsales task filter. Use one documented filter at a time, such as open, due_today, due_tomorrow, overdue, or completed. Default: `open`. Example: `open`. |
| `page` | number | no | Page number to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDate": "string",
      "createdAt": "string",
      "createrId": 1,
      "description": "string",
      "dueDate": "string",
      "hasMultipleEmails": true,
      "id": 1,
      "isLinkedinType": true,
      "outcomeId": 1,
      "ownerId": 1,
      "status": 1,
      "targetables": [
        {}
      ],
      "targetablesWithEmail": [
        {}
      ],
      "taskTypeId": 1,
      "title": "string",
      "updatedAt": "string",
      "updaterId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedDate` | string |  |
| `createdAt` | string |  |
| `createrId` | number |  |
| `description` | string |  |
| `dueDate` | string |  |
| `hasMultipleEmails` | boolean |  |
| `id` | number |  |
| `isLinkedinType` | boolean |  |
| `outcomeId` | number |  |
| `ownerId` | number |  |
| `status` | number |  |
| `targetables` | array<object> |  |
| `targetablesWithEmail` | array<object> |  |
| `taskTypeId` | number |  |
| `title` | string |  |
| `updatedAt` | string |  |
| `updaterId` | number |  |

## Native endpoint

Through the native Freshsales Classic API, this operation is `GET /tasks` (base URL `https://{{credentials.bundleAlias}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-all-tasks.md) for the provider-specific parameters and requirements.

