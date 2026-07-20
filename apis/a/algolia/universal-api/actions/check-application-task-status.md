# Algolia: Check Application Task Status

Retrieves an application task status from Algolia.

```
GET https://connect.mindcloud.co/v1/universal/algolia/latest/actions/check-application-task-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Algolia `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/algolia/latest/actions/check-application-task-status?connectionId=$CONNECTION_ID&taskID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "taskID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/algolia/latest/actions/check-application-task-status?${params}`, {
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
| `taskID` | number | yes | The application task identifier returned by a multi-index or settings operation. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Algolia API returns.

## Native endpoint

Through the native Algolia API, this operation is `GET /1/task/:taskID` (base URL `https://{{credentials.applicationId}}.algolia.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-application-task-status.md) for the provider-specific parameters and requirements.

