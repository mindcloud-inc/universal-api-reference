# Feathery: Delete a Form



```
DELETE https://connect.mindcloud.co/v1/universal/feathery/latest/actions/delete-a-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/delete-a-form?connectionId=$CONNECTION_ID&form_id=string&confirm_delete=true" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "form_id": "string",
  "confirm_delete": "true"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/delete-a-form?${params}`, {
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
| `form_id` | string | yes | The ID of the form to delete. |
| `confirm_delete` | boolean | yes | Set to true to confirm deletion of the form. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Feathery API returns.

## Native endpoint

Through the native Feathery API, this operation is `DELETE /api/form/:form_id/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-a-form.md) for the provider-specific parameters and requirements.

