# FTrack: Delete Delayed Job

Deletes a delayed job from FTrack.

```
DELETE https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/delete-delayed-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FTrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/delete-delayed-job?connectionId=$CONNECTION_ID&data=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fTrack/latest/actions/delete-delayed-job?${params}`, {
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
| `data` | object | yes | Delayed job data payload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native FTrack API returns.

## Native endpoint

Through the native FTrack API, this operation is `POST /api` (base URL `{{credentials.serverUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-delayed-job.md) for the provider-specific parameters and requirements.

