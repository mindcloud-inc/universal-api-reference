# Storyscale: Delete Library Asset



```
DELETE https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/delete-library-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Storyscale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/delete-library-asset?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyscale/latest/actions/delete-library-asset?${params}`, {
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
| `id` | string | yes | The Storyscale library asset ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "status": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Delete result returned by Storyscale. |
| `status` | object | Top-level API status object. |

## Native endpoint

Through the native Storyscale API, this operation is `DELETE /v1/library/delete/{id}` (base URL `https://prodapi.storyscale.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-library-asset.md) for the provider-specific parameters and requirements.

