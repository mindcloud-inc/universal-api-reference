# Innform: Create Assignment

Assigns a training item to a user in Innform.

```
POST https://connect.mindcloud.co/v1/universal/innform/latest/actions/create-assignment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Innform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/innform/latest/actions/create-assignment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/innform/latest/actions/create-assignment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "string",
    "userId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dueDate` | date | no | Optional assignment due date. |
| `itemId` | string | yes | Course or learning path UUID to assign. |
| `itemType` | string | no | Optional item type such as LearningPath. One of: `0`. |
| `userId` | string | yes | User UUID to assign. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Innform API returns.

## Native endpoint

Through the native Innform API, this operation is `POST /assignments` (base URL `https://api.innform.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-assignment.md) for the provider-specific parameters and requirements.

