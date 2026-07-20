# Rulebricks: Delete Context

Deletes a context from Rulebricks.

```
DELETE https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/delete-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rulebricks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/delete-context?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rulebricks/latest/actions/delete-context?${params}`, {
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
| `id` | string | yes | ID of the context to delete |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Deletion result message |

## Native endpoint

Through the native Rulebricks API, this operation is `DELETE /admin/contexts/:id` (base URL `https://rulebricks.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-context.md) for the provider-specific parameters and requirements.

