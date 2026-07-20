# ClickUp: List Folders

View the Folders in a Space.

```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-folders?connectionId=$CONNECTION_ID&spaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "spaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-folders?${params}`, {
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
| `spaceId` | string | yes |  |
| `archived` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "hidden": true,
      "id": "string",
      "lists": [
        {
          "archived": true,
          "assignee": "string",
          "dueDate": "string",
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
          "statuses": [
            {
              "color": "string",
              "id": "string",
              "orderindex": 1,
              "status": "string",
              "statusGroup": "string",
              "type": "string"
            }
          ],
          "taskCount": 1
        }
      ],
      "name": "Ava Chen",
      "orderindex": 1,
      "overrideStatuses": true,
      "permissionLevel": "string",
      "space": {
        "id": "string",
        "name": "Ava Chen"
      },
      "taskCount": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `hidden` | boolean |  |
| `id` | string |  |
| `lists[].archived` | boolean |  |
| `lists[].assignee` | string |  |
| `lists[].dueDate` | string |  |
| `lists[].id` | string |  |
| `lists[].name` | string |  |
| `lists[].orderindex` | number |  |
| `lists[].overrideStatuses` | boolean |  |
| `lists[].permissionLevel` | string |  |
| `lists[].priority` | string |  |
| `lists[].space.access` | boolean |  |
| `lists[].space.id` | string |  |
| `lists[].space.name` | string |  |
| `lists[].startDate` | string |  |
| `lists[].status` | string |  |
| `lists[].statuses[].color` | string |  |
| `lists[].statuses[].id` | string |  |
| `lists[].statuses[].orderindex` | number |  |
| `lists[].statuses[].status` | string |  |
| `lists[].statuses[].statusGroup` | string |  |
| `lists[].statuses[].type` | string |  |
| `lists[].taskCount` | number |  |
| `name` | string |  |
| `orderindex` | number |  |
| `overrideStatuses` | boolean |  |
| `permissionLevel` | string |  |
| `space.id` | string |  |
| `space.name` | string |  |
| `taskCount` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET space/:space_id/folder` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-folders.md) for the provider-specific parameters and requirements.

