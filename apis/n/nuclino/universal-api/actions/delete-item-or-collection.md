# Nuclino: Delete item or collection

Deletes an existing item or collection from Nuclino.

```
DELETE https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/delete-item-or-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nuclino `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/delete-item-or-collection?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nuclino/latest/actions/delete-item-or-collection?${params}`, {
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
| `id` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Nuclino API returns.

## Native endpoint

Through the native Nuclino API, this operation is `DELETE /items/:id` (base URL `https://api.nuclino.com/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-item-or-collection.md) for the provider-specific parameters and requirements.

