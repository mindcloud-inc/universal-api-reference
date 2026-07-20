# Temi: Delete Job

Deletes a transcription job from Temi.

```
DELETE https://connect.mindcloud.co/v1/universal/temi/latest/actions/delete-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Temi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/temi/latest/actions/delete-job?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/temi/latest/actions/delete-job?${params}`, {
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
| `id` | string | yes | Temi job identifier to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Temi API returns.

## Native endpoint

Through the native Temi API, this operation is `DELETE /jobs/:id` (base URL `https://api.temi.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-job.md) for the provider-specific parameters and requirements.

