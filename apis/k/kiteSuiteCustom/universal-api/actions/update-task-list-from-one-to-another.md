# Kite Suite: Update task List from one to another



```
PUT https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-task-list-from-one-to-another
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kite Suite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-task-list-from-one-to-another" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "newListID": "string",
  "position": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/kiteSuiteCustom/latest/actions/update-task-list-from-one-to-another', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "newListID": "string",
    "position": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | Request body |
| `id` | string | no | Task ID |
| `newListID` | string | yes |  |
| `position` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "listName": "Ava Chen",
      "order": 1,
      "projectID": "string",
      "status": "string",
      "tasks": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | ID of the list |
| `listName` | string | list name |
| `order` | number | order number |
| `projectID` | string | project ID of project |
| `status` | string | status of list |
| `tasks` | array | task of this project |

## Native endpoint

Through the native Kite Suite API, this operation is `PATCH /api/v1/list/task/:id` (base URL `https://api.kitesuite.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-list-from-one-to-another.md) for the provider-specific parameters and requirements.

