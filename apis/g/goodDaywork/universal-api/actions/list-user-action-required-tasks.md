# GoodDay.work: List User Action Required Tasks

Finds tasks requiring action from a GoodDay.work user.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-user-action-required-tasks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-user-action-required-tasks?connectionId=$CONNECTION_ID&userId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-user-action-required-tasks?${params}`, {
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
| `userId` | string | yes | GoodDay user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedToUserId": "string",
      "id": "string",
      "name": "Ava Chen",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedToUserId` | string | Assigned user ID. |
| `id` | string | Task ID. |
| `name` | string | Task title. |
| `projectId` | string | Associated project ID. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /user/:userId/action-required-tasks` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-action-required-tasks.md) for the provider-specific parameters and requirements.

