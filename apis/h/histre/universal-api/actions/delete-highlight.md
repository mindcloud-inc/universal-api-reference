# Histre: Delete Highlight

Deletes a highlight from Histre.

```
DELETE https://connect.mindcloud.co/v1/universal/histre/latest/actions/delete-highlight
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Histre `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/histre/latest/actions/delete-highlight?connectionId=$CONNECTION_ID&highlightId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "highlightId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/histre/latest/actions/delete-highlight?${params}`, {
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
| `highlightId` | string | yes | Identifier of the highlight to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Histre API returns.

## Native endpoint

Through the native Histre API, this operation is `DELETE /api/v1/highlight/` (base URL `https://histre.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-highlight.md) for the provider-specific parameters and requirements.

