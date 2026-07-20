# Quire: List Root Tasks

Retrieves root tasks from a Quire project.

```
GET https://connect.mindcloud.co/v1/universal/quire/latest/actions/list-root-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Quire `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quire/latest/actions/list-root-tasks?connectionId=$CONNECTION_ID&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "projectId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quire/latest/actions/list-root-tasks?${params}`, {
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
| `projectId` | string | yes | ID of the project whose root tasks should be returned. |

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
| `partnerBy` | object |  |
| `priority` | object |  |
| `status` | object |  |
| `tags` | array<object> |  |
| `toggledBy` | object |  |
| `url` | string |  |

## Native endpoint

Through the native Quire API, this operation is `GET task/list/id/:projectId` (base URL `https://quire.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-root-tasks.md) for the provider-specific parameters and requirements.

