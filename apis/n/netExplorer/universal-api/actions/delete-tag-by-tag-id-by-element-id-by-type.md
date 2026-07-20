# NetExplorer: Delete Tag



```
DELETE https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-tag-by-tag-id-by-element-id-by-type
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NetExplorer `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-tag-by-tag-id-by-element-id-by-type?connectionId=$CONNECTION_ID&tagId=string&elementId=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tagId": "string",
  "elementId": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netExplorer/latest/actions/delete-tag-by-tag-id-by-element-id-by-type?${params}`, {
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
| `tagId` | string | yes |  |
| `elementId` | string | yes |  |
| `type` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native NetExplorer API returns.

## Native endpoint

Through the native NetExplorer API, this operation is `DELETE /tag/:tagId/:elementId/:type` (base URL `{{credentials.platformBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tag-by-tag-id-by-element-id-by-type.md) for the provider-specific parameters and requirements.

