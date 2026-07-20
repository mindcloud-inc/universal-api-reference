# KYVE: List Finalized Bundles



```
GET https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/list-finalized-bundles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a KYVE `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/list-finalized-bundles?connectionId=$CONNECTION_ID&limit=25&offset=0&poolId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "poolId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kYVE/latest/actions/list-finalized-bundles?${params}`, {
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
| `poolId` | string | yes | Pool ID to list finalized bundles for. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `index` | string | no | Optional bundle index filter; cannot be combined with pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "finalized_bundles": [
        {}
      ],
      "pagination": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `finalized_bundles` | array<object> |  |
| `pagination` | object |  |

## Native endpoint

Through the native KYVE API, this operation is `GET /kyve/v1/bundles/{pool_id}` (base URL `https://api.kyve.network`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-finalized-bundles.md) for the provider-specific parameters and requirements.

