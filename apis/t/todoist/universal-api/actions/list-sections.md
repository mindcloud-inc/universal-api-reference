# Todoist: List Sections

Retrieves sections from Todoist.

```
GET https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-sections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-sections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/todoist/latest/actions/list-sections?${params}`, {
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
| `projectId` | string | no | Optional project ID to return sections for a specific project. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cursor` | string | no | Cursor for the next page of results. |
| `limit` | number | no | Maximum number of results to return. |
| `publicKey` | string | no | Public key used for shared-resource access where applicable. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addedAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "isArchived": true,
      "isCollapsed": true,
      "isDeleted": true,
      "name": "Ava Chen",
      "projectId": "string",
      "sectionOrder": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addedAt` | date | Creation timestamp |
| `id` | string | Section ID |
| `isArchived` | boolean | Whether section is archived |
| `isCollapsed` | boolean | Whether section is collapsed |
| `isDeleted` | boolean | Whether section is deleted |
| `name` | string | Section name |
| `projectId` | string | Parent project ID |
| `sectionOrder` | number | Section display order |
| `updatedAt` | date | Last update timestamp |

## Native endpoint

Through the native Todoist API, this operation is `GET /api/v1/sections` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sections.md) for the provider-specific parameters and requirements.

