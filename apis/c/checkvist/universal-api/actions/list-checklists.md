# Checkvist: List Checklists

Retrieves checklists from Checkvist.

```
GET https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/list-checklists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Checkvist `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/list-checklists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/checkvist/latest/actions/list-checklists?${params}`, {
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
| `archived` | boolean | no | Return archived checklists. |
| `order` | string | no | Sort checklists, for example updated_at:asc or id:desc. |
| `skipStats` | boolean | no | Skip checklist user and task stats for a faster response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "string",
      "id": 1,
      "itemCount": 1,
      "name": "Ava Chen",
      "options": 1,
      "percentCompleted": 1,
      "public": true,
      "readOnly": true,
      "tags": {},
      "tagsAsText": "string",
      "taskCompleted": 1,
      "taskCount": 1,
      "updatedAt": "string",
      "userCount": 1,
      "userUpdatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the checklist is archived. |
| `createdAt` | string | When the checklist was created. |
| `id` | number | The checklist ID. |
| `itemCount` | number | The total number of checklist items. |
| `name` | string | The checklist name. |
| `options` | number | The checklist options bitmask. |
| `percentCompleted` | number | The percent of completed tasks. |
| `public` | boolean | Whether the checklist is public. |
| `readOnly` | boolean | Whether the checklist is read-only. |
| `tags` | object | Checklist tags keyed by tag name. |
| `tagsAsText` | string | The checklist tags as plain text. |
| `taskCompleted` | number | The number of completed tasks. |
| `taskCount` | number | The total number of tasks. |
| `updatedAt` | string | When the checklist was last updated. |
| `userCount` | number | How many users are on the checklist. |
| `userUpdatedAt` | string | When the current user's checklist state was updated. |

## Native endpoint

Through the native Checkvist API, this operation is `GET /checklists.json` (base URL `https://checkvist.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-checklists.md) for the provider-specific parameters and requirements.

