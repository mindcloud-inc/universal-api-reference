# Cloudinary: Delete Resources by Asset IDs

Deletes Cloudinary resources by asset IDs.

```
DELETE https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/delete-resources-by-asset-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloudinary `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/delete-resources-by-asset-ids?connectionId=$CONNECTION_ID&asset_ids%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "asset_ids[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudinary/latest/actions/delete-resources-by-asset-ids?${params}`, {
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
| `asset_ids[]` | array<string> | yes | The asset IDs to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deleted": {},
      "deleted_counts": {},
      "partial": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deleted` | object |  |
| `deleted_counts` | object |  |
| `partial` | boolean |  |

## Native endpoint

Through the native Cloudinary API, this operation is `DELETE /resources` (base URL `https://api.cloudinary.com/v1_1/{{credentials.cloudName}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-resources-by-asset-ids.md) for the provider-specific parameters and requirements.

