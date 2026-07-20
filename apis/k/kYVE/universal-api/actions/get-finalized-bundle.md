# KYVE: Get Finalized Bundle



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-finalized-bundle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-finalized-bundle?connectionId=$CONNECTION_ID&poolId=string&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "poolId": "string",
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/get-finalized-bundle?${params}`, {
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
| `poolId` | string | yes | Pool ID for the finalized bundle. |
| `id` | string | yes | Finalized bundle ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bundle_summary": "string",
      "compression_id": "string",
      "data_hash": "string",
      "finalized_at": {},
      "from_index": "string",
      "from_key": "string",
      "id": "string",
      "pool_id": "string",
      "stake_security": {},
      "storage_id": "string",
      "storage_provider_id": "string",
      "to_index": "string",
      "to_key": "string",
      "uploader": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bundle_summary` | string |  |
| `compression_id` | string |  |
| `data_hash` | string |  |
| `finalized_at` | object |  |
| `from_index` | string |  |
| `from_key` | string |  |
| `id` | string |  |
| `pool_id` | string |  |
| `stake_security` | object |  |
| `storage_id` | string |  |
| `storage_provider_id` | string |  |
| `to_index` | string |  |
| `to_key` | string |  |
| `uploader` | string |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/v1/bundles/{pool_id}/{id}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-finalized-bundle.md) for the provider-specific parameters and requirements.

