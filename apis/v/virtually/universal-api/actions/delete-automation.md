# Virtually: Delete Automation

Deletes an existing automation from Virtually.

```
DELETE https://connect.mindcloud.co/v1/universal/virtually/latest/actions/delete-automation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Virtually `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/virtually/latest/actions/delete-automation?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/virtually/latest/actions/delete-automation?${params}`, {
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
| `id` | string | yes | The automation ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Virtually API returns.

## Native endpoint

Through the native Virtually API, this operation is `DELETE /api/v2/orgs/:orgId/automations/:id` (base URL `https://app.tryvirtually.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-automation.md) for the provider-specific parameters and requirements.

