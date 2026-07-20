# Clockify: Publish Assignments

Publishes workspace scheduling assignments in Clockify.

```
PUT https://connect.mindcloud.co/v1/universal/clockify/latest/actions/publish-assignments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clockify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/clockify/latest/actions/publish-assignments" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "end": "string",
  "start": "string",
  "workspaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/clockify/latest/actions/publish-assignments', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "end": "string",
    "start": "string",
    "workspaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `end` | string | yes |  |
| `notifyUsers` | boolean | no |  |
| `search` | string | no |  |
| `start` | string | yes |  |
| `userFilter` | object | no |  |
| `userFilter.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userFilter.ids[]` | array<string> | no |  |
| `userFilter.sourceType` | list | no | One of: `USER_GROUP`. |
| `userFilter.status` | list | no | One of: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `userFilter.statuses` | list<string> | no | One of: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. Accepts multiple values as an array. |
| `userGroupFilter` | object | no |  |
| `userGroupFilter.contains` | list | no | One of: `CONTAINS`, `CONTAINS_ONLY`, `DOES_NOT_CONTAIN`. |
| `userGroupFilter.ids[]` | array<string> | no |  |
| `userGroupFilter.status` | list | no | One of: `ACTIVE`, `ALL`, `DECLINED`, `INACTIVE`, `PENDING`. |
| `viewType` | list | no | One of: `ALL`, `PROJECTS`, `TEAM`. |
| `workspaceId` | list<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "start": "2026-05-07T12:00:00.000Z",
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date | The end of the published schedule window. |
| `start` | date | The start of the published schedule window. |
| `workspaceId` | string | The workspace where assignments were published. |

## Native endpoint

Through the native Clockify API, this operation is `PUT workspaces/:workspaceId/scheduling/assignments/publish` (base URL `https://api.clockify.me/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-assignments.md) for the provider-specific parameters and requirements.

