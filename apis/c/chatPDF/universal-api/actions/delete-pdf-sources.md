# ChatPDF: Delete PDF Sources



```
DELETE https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/delete-pdf-sources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChatPDF `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/delete-pdf-sources?connectionId=$CONNECTION_ID&sources%5B%5D=src_xxxxxx" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sources[]": "src_xxxxxx"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chatPDF/latest/actions/delete-pdf-sources?${params}`, {
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
| `sources[]` | array<string> | yes | Array of ChatPDF source IDs to delete. Example: `src_xxxxxx`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ChatPDF API returns.

## Native endpoint

Through the native ChatPDF API, this operation is `POST /sources/delete` (base URL `https://api.chatpdf.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-pdf-sources.md) for the provider-specific parameters and requirements.

