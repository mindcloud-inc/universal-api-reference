# Mux: Delete an Asset



```
DELETE https://connect.mindcloud.co/v1/universal/mux/latest/actions/delete-an-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mux/latest/actions/delete-an-asset?connectionId=$CONNECTION_ID&assetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "assetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mux/latest/actions/delete-an-asset?${params}`, {
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
| `assetId` | string | yes | The Mux asset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean |  |

## Native endpoint

Through the native Mux API, this operation is `DELETE /video/v1/assets/{ASSET_ID}` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-an-asset.md) for the provider-specific parameters and requirements.

