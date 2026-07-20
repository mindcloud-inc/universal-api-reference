# Voog: Delete Asset

Deletes an existing asset from the current Voog site.

```
DELETE https://connect.mindcloud.co/v1/universal/voog/latest/actions/delete-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/voog/latest/actions/delete-asset?connectionId=$CONNECTION_ID&assetId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/voog/latest/actions/delete-asset?${params}`, {
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
| `assetId` | number | yes | Numeric asset ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voog API returns.

## Native endpoint

Through the native Voog API, this operation is `DELETE /assets/:assetId` (base URL `{{credentials.siteUrl}}/admin/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-asset.md) for the provider-specific parameters and requirements.

