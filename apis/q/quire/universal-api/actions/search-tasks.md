# Quire: Search Tasks

Finds tasks in a Quire project by search text.

```
GET https://connect.mindcloud.co/v1/universal/quire/latest/actions/search-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quire/latest/actions/search-tasks?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quire/latest/actions/search-tasks?${params}`, {
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
| `projectId` | string | yes | The project ID or shortcut, for example App_Account. |
| `text` | string | no | Task title text to search for within the project. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archivedBy": {},
      "assignees": [
        {}
      ],
      "assignors": [
        {}
      ],
      "attachments": [
        {}
      ],
      "childCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "description": "string",
      "descriptionHtml": "string",
      "descriptionText": "string",
      "favorites": [
        {}
      ],
      "followers": [
        {}
      ],
      "id": 1,
      "mutes": [
        {}
      ],
      "name": "Ava Chen",
      "nameHtml": "Ava Chen",
      "nameText": "Ava Chen",
      "oid": "string",
      "parent": {},
      "partnerBy": {},
      "priority": {},
      "status": {},
      "tags": [
        {}
      ],
      "toggledBy": {},
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archivedBy` | object |  |
| `assignees` | array<object> |  |
| `assignors` | array<object> |  |
| `attachments` | array<object> |  |
| `childCount` | number |  |
| `createdAt` | date |  |
| `createdBy` | object |  |
| `description` | string |  |
| `descriptionHtml` | string |  |
| `descriptionText` | string |  |
| `favorites` | array<object> |  |
| `followers` | array<object> |  |
| `id` | number |  |
| `mutes` | array<object> |  |
| `name` | string |  |
| `nameHtml` | string |  |
| `nameText` | string |  |
| `oid` | string |  |
| `parent` | object |  |
| `partnerBy` | object |  |
| `priority` | object |  |
| `status` | object |  |
| `tags` | array<object> |  |
| `toggledBy` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Quire API, this operation is `GET task/search/id/:projectId` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-tasks.md) for the provider-specific parameters and requirements.

