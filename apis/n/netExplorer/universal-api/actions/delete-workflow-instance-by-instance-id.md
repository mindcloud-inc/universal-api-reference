# NetExplorer: Delete Instance



```
DELETE https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-workflow-instance-by-instance-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-workflow-instance-by-instance-id?connectionId=$CONNECTION_ID&instanceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "instanceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-workflow-instance-by-instance-id?${params}`, {
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
| `instanceId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetExplorer API returns.

## Native endpoint

Through the native NetExplorer API, this operation is `DELETE /workflow/instance/:instanceId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-workflow-instance-by-instance-id.md) for the provider-specific parameters and requirements.

