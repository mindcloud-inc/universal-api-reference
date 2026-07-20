# Melo: Delete Search

Deletes an existing search from Melo.

```
DELETE https://connect.mindcloud.co/v1/universal/melo/latest/actions/delete-search
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Melo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/melo/latest/actions/delete-search?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/melo/latest/actions/delete-search?${params}`, {
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
| `id` | string | yes | Search resource identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Melo API returns.

## Native endpoint

Through the native Melo API, this operation is `DELETE /searches/:id` (base URL `https://preprod-api.notif.immo`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-search.md) for the provider-specific parameters and requirements.

