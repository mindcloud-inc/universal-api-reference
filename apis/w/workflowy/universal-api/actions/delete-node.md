# Workflowy: Delete Node

Deletes an existing node from Workflowy.

```
DELETE https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/delete-node
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Workflowy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/delete-node?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/workflowy/latest/actions/delete-node?${params}`, {
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
| `id` | string | yes | The identifier of the node to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Workflowy operation status. |

## Native endpoint

Through the native Workflowy API, this operation is `DELETE /nodes/:id` (base URL `https://workflowy.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-node.md) for the provider-specific parameters and requirements.

