# Lemcal: Delete Hook

Deletes an existing hook from Lemcal.

```
DELETE https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/delete-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lemcal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/delete-hook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemcal/latest/actions/delete-hook?${params}`, {
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
| `id` | string | yes | The ID of the hook to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Lemcal API returns.

## Native endpoint

Through the native Lemcal API, this operation is `DELETE /hooks/:id` (base URL `https://api.lemcal.com/api/lemcal`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-hook.md) for the provider-specific parameters and requirements.

