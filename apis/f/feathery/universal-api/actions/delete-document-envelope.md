# Feathery: Delete Document Envelope



```
DELETE https://connect.mindcloud.co/v1/universal/feathery/latest/actions/delete-document-envelope
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Feathery `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/feathery/latest/actions/delete-document-envelope?connectionId=$CONNECTION_ID&envelope_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "envelope_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/feathery/latest/actions/delete-document-envelope?${params}`, {
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
| `envelope_id` | string | yes | The ID of the envelope to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Feathery API returns.

## Native endpoint

Through the native Feathery API, this operation is `DELETE /api/document/envelope/:envelope_id/` (base URL `https://api.feathery.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document-envelope.md) for the provider-specific parameters and requirements.

