# Instafill: Delete Power Automate Hook



```
DELETE https://connect.mindcloud.co/v1/universal/instafill/latest/actions/delete-power-automate-hook
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instafill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/instafill/latest/actions/delete-power-automate-hook?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instafill/latest/actions/delete-power-automate-hook?${params}`, {
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

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Instafill API returns.

## Native endpoint

Through the native Instafill API, this operation is `DELETE /v1/integrations/power-automate/hooks/:id` (base URL `https://api.instafill.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-power-automate-hook.md) for the provider-specific parameters and requirements.

