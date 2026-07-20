# ClickUp: Get List



```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/get-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/get-list?connectionId=$CONNECTION_ID&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/get-list?${params}`, {
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
| `listId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "assignee": "string",
      "dueDate": "string",
      "folder": {
        "access": true,
        "hidden": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "id": "string",
      "name": "Ava Chen",
      "orderindex": 1,
      "overrideStatuses": true,
      "permissionLevel": "string",
      "priority": "string",
      "space": {
        "access": true,
        "id": "string",
        "name": "Ava Chen"
      },
      "startDate": "string",
      "status": "string",
      "taskCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `assignee` | string |  |
| `dueDate` | string |  |
| `folder.access` | boolean |  |
| `folder.hidden` | boolean |  |
| `folder.id` | string |  |
| `folder.name` | string |  |
| `id` | string |  |
| `name` | string |  |
| `orderindex` | number |  |
| `overrideStatuses` | boolean |  |
| `permissionLevel` | string |  |
| `priority` | string |  |
| `space.access` | boolean |  |
| `space.id` | string |  |
| `space.name` | string |  |
| `startDate` | string |  |
| `status` | string |  |
| `taskCount` | number |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET list/:list_id` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list.md) for the provider-specific parameters and requirements.

