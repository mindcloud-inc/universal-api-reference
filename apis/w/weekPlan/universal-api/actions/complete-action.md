# Week Plan: Complete Action



```
PUT https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/complete-action
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Week Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/complete-action" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ActionId": 1,
  "IsCompleted": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekPlan/latest/actions/complete-action', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ActionId": 1,
    "IsCompleted": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ActionId` | number | yes | The action to complete or reopen. |
| `IsCompleted` | boolean | yes | Whether the action should be marked complete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ActionId": 1,
      "CompletedAt": 1,
      "IsCompleted": true,
      "JournalLogs": [
        {}
      ],
      "Text": "string",
      "WorkspaceId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ActionId` | number |  |
| `CompletedAt` | number |  |
| `IsCompleted` | boolean |  |
| `JournalLogs` | array<object> |  |
| `Text` | string |  |
| `WorkspaceId` | number |  |

## Native endpoint

Through the native Week Plan API, this operation is `POST actions/complete` (base URL `https://api.weekplan.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/complete-action.md) for the provider-specific parameters and requirements.

