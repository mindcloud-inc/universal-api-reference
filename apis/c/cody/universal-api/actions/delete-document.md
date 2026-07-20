# Cody: Delete Document



```
DELETE https://connect.mindcloud.co/v1/universal/cody/latest/actions/delete-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cody `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cody/latest/actions/delete-document?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cody/latest/actions/delete-document?${params}`, {
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
| `id` | string | yes | Id of the document. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cody API returns.

## Native endpoint

Through the native Cody API, this operation is `DELETE /documents/:id` (base URL `https://getcody.ai/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-document.md) for the provider-specific parameters and requirements.

