# EasyPost: List Batches

Retrieves a list of batches from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-batches
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-batches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-batches?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "labelUrl": "https://example.com",
      "mode": "string",
      "numShipments": 1,
      "object": "string",
      "scanForm": {},
      "shipments": [
        {}
      ],
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `labelUrl` | string |  |
| `mode` | string |  |
| `numShipments` | number |  |
| `object` | string |  |
| `scanForm` | object |  |
| `shipments` | array<object> |  |
| `state` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `GET /batches` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-batches.md) for the provider-specific parameters and requirements.

