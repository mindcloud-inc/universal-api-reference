# Tinq.ai: List Datasource Documents



```
GET https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/list-datasource-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tinq.ai `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/list-datasource-documents?connectionId=$CONNECTION_ID&datasource=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "datasource": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tinqai/latest/actions/list-datasource-documents?${params}`, {
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
| `datasource` | string | yes | Datasource ID to list documents from. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Tinq.ai API returns.

## Native endpoint

Through the native Tinq.ai API, this operation is `GET /api/v2/datasources/documents` (base URL `https://tinq.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-datasource-documents.md) for the provider-specific parameters and requirements.

