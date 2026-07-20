# Algolia: Check Task Status

Retrieves a task status from Algolia.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/check-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/check-task-status?connectionId=$CONNECTION_ID&indexName=Ava%20Chen&taskID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "indexName": "Ava Chen",
  "taskID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/check-task-status?${params}`, {
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
| `indexName` | string | yes | The name of the Algolia index. |
| `taskID` | number | yes | The task identifier returned by an index operation. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "pendingTask": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `pendingTask` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Algolia API, this operation is `GET /1/indexes/:indexName/task/:taskID` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-task-status.md) for the provider-specific parameters and requirements.

