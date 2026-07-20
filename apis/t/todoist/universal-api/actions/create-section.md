# Todoist: Create Section

Creates a new section in Todoist.

```
POST https://connect.mindcloud.co/v1/universal/todoist/latest/actions/create-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Todoist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/todoist/latest/actions/create-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "projectId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/todoist/latest/actions/create-section', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "projectId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Section name. |
| `projectId` | string | yes | Project ID where the section will be created. |
| `order` | number | no | Custom section order value. |

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

Through the native Todoist API, this operation is `POST /api/v1/sections` (base URL `https://api.todoist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-section.md) for the provider-specific parameters and requirements.

