# NetExplorer: Delete File



```
DELETE https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-sharelink-by-sharelink-id-file-by-file-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-sharelink-by-sharelink-id-file-by-file-id?connectionId=$CONNECTION_ID&sharelinkId=https%3A%2F%2Fexample.com&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sharelinkId": "https://example.com",
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-sharelink-by-sharelink-id-file-by-file-id?${params}`, {
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
| `sharelinkId` | string | yes |  |
| `fileId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetExplorer API returns.

## Native endpoint

Through the native NetExplorer API, this operation is `DELETE /sharelink/:sharelinkId/file/:fileId` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-sharelink-by-sharelink-id-file-by-file-id.md) for the provider-specific parameters and requirements.

