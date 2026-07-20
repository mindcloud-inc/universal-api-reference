# Wrangle: Update Inbox



```
PUT https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/update-inbox
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrangle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/update-inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inboxId": "inbox_uuid"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrangle/latest/actions/update-inbox', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inboxId": "inbox_uuid"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inboxId` | string | yes | The Wrangle inbox ID. Example: `inbox_uuid`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userRoles.NO_ACCESS[]` | array<string> | no | Slack user IDs to assign the No Access role for this inbox. |
| `userRoles.REQUESTER[]` | array<string> | no | Slack user IDs to assign the Requester role for this inbox. |
| `userRoles.OBSERVER[]` | array<string> | no | Slack user IDs to assign the Observer role for this inbox. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "inbox": {
        "createdAt": "string",
        "creatorId": "string",
        "defaultUserRole": "string",
        "description": {},
        "id": "string",
        "name": "Ava Chen",
        "status": "string",
        "updatedAt": "string",
        "userRoles": [
          {
            "role": "string",
            "userId": "string"
          }
        ]
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `inbox.createdAt` | string |  |
| `inbox.creatorId` | string |  |
| `inbox.defaultUserRole` | string |  |
| `inbox.description` | object |  |
| `inbox.id` | string |  |
| `inbox.name` | string |  |
| `inbox.status` | string |  |
| `inbox.updatedAt` | string |  |
| `inbox.userRoles[].role` | string |  |
| `inbox.userRoles[].userId` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Wrangle API, this operation is `PUT /inboxes/:inboxId` (base URL `https://slack.wrangle.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inbox.md) for the provider-specific parameters and requirements.

