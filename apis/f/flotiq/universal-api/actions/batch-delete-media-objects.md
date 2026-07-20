# Flotiq: Batch Delete Media Objects

Deletes multiple media objects from Flotiq.

```
DELETE https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/batch-delete-media-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/batch-delete-media-objects?connectionId=$CONNECTION_ID&body=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "body": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/batch-delete-media-objects?${params}`, {
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
| `body` | object | yes | The batch delete payload for media objects. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Flotiq API returns.

## Native endpoint

Through the native Flotiq API, this operation is `POST /content/_media/batch-delete` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-delete-media-objects.md) for the provider-specific parameters and requirements.

