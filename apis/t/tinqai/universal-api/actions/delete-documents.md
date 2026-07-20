# Tinq.ai: Delete Documents



```
DELETE https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/delete-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/delete-documents?connectionId=$CONNECTION_ID&documents%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documents[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/delete-documents?${params}`, {
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
| `documents[]` | array<string> | yes | One or more document slugs to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tinq.ai API returns.

## Native endpoint

Through the native Tinq.ai API, this operation is `DELETE /api/v2/documents/delete` (base URL `https://tinq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-documents.md) for the provider-specific parameters and requirements.

