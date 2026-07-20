# Flotiq: Batch Delete Content Objects

Deletes multiple content objects from Flotiq.

```
DELETE https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/batch-delete-content-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/batch-delete-content-objects?connectionId=$CONNECTION_ID&name=Ava%20Chen&body=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen",
  "body": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/batch-delete-content-objects?${params}`, {
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
| `name` | string | yes | The content type name that owns the objects. |
| `body` | object | yes | The batch delete payload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Flotiq API returns.

## Native endpoint

Through the native Flotiq API, this operation is `POST /content/{{name}}/batch-delete` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-delete-content-objects.md) for the provider-specific parameters and requirements.

