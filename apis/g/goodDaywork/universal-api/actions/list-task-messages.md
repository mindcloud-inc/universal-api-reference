# GoodDay.work: List Task Messages

Finds messages on a GoodDay.work task.

```
GET https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-task-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoodDay.work `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-task-messages?connectionId=$CONNECTION_ID&taskId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodDaywork/latest/actions/list-task-messages?${params}`, {
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
| `taskId` | string | yes | GoodDay task ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "momentCreated": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Message ID. |
| `message` | string | Message body. |
| `momentCreated` | string | Creation timestamp. |
| `userId` | string | Author user ID. |

## Native endpoint

Through the native GoodDay.work API, this operation is `GET /task/:taskId/messages` (base URL `https://api.goodday.work/2.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-messages.md) for the provider-specific parameters and requirements.

