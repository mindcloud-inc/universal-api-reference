# AppWright: Update Task Date

Updates a job task due date in AppWright.

```
PUT https://connect.mindcloud.co/v1/universal/appWright/latest/actions/update-task-date
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a AppWright `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/appWright/latest/actions/update-task-date" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/appWright/latest/actions/update-task-date', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `JobNumber` | string | no |  |
| `TaskDesc` | string | no |  |
| `DueDate` | string | no |  |
| `MoveOption` | list | no | Example: `B`. |
| `Status` | list | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native AppWright API returns.

## Native endpoint

Through the native AppWright API, this operation is `POST awAPI/awAPI.asp` (base URL `https://{{credentials.clientId}}.AppWright.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-task-date.md) for the provider-specific parameters and requirements.

