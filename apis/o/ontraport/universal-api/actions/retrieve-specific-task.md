# Ontraport: Retrieve Specific Task

Retrieves a specific task from Ontraport.

```
GET https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-specific-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ontraport `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-specific-task?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ontraport/latest/actions/retrieve-specific-task?${params}`, {
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
| `id` | number | yes | The task ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ontraport API returns.

## Native endpoint

Through the native Ontraport API, this operation is `GET /Task` (base URL `https://api.ontraport.com/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-specific-task.md) for the provider-specific parameters and requirements.

