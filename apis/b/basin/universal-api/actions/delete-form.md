# Basin: Delete Form

Deletes an existing form from Basin.

```
DELETE https://connect.mindcloud.co/v1/universal/basin/latest/actions/delete-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Basin `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/basin/latest/actions/delete-form?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basin/latest/actions/delete-form?${params}`, {
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
| `id` | string | yes | ID of the form to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Basin API returns.

## Native endpoint

Through the native Basin API, this operation is `DELETE /api/v1/forms/:id` (base URL `https://usebasin.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-form.md) for the provider-specific parameters and requirements.

