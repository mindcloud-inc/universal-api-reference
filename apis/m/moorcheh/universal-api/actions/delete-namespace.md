# Moorcheh: Delete Namespace

Deletes a namespace and its data from Moorcheh.

```
DELETE https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/delete-namespace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Moorcheh `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/delete-namespace?connectionId=$CONNECTION_ID&namespace_name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "namespace_name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moorcheh/latest/actions/delete-namespace?${params}`, {
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
| `namespace_name` | string | yes | Name of the namespace to permanently delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Human-readable deletion queue message. |
| `status` | string | Namespace deletion request status. |

## Native endpoint

Through the native Moorcheh API, this operation is `DELETE /namespaces/:namespace_name` (base URL `https://api.moorcheh.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-namespace.md) for the provider-specific parameters and requirements.

