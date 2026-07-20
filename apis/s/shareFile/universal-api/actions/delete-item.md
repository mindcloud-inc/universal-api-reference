# ShareFile: Delete Item



```
DELETE https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/delete-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ShareFile `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/delete-item?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shareFile/latest/actions/delete-item?${params}`, {
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
| `id` | string | yes | The ShareFile item identifier to delete. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ShareFile API returns.

## Native endpoint

Through the native ShareFile API, this operation is `DELETE /Items({{id}})` (base URL `https://{{credentials.accessTokenRequest.subdomain}}.{{credentials.accessTokenRequest.apicp}}/sf/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-item.md) for the provider-specific parameters and requirements.

