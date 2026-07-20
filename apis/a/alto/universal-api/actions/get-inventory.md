# Alto: Get Inventory

Retrieves inventory records from your Alto account.

```
GET https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Alto `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alto/latest/actions/get-inventory?${params}`, {
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
| `address` | string | no | Address text to filter inventory results. |
| `category` | string | no | Inventory category filter. |
| `recordType` | string | no | Inventory record type filter. |
| `archived` | boolean | no | Whether to include archived inventory records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `id` | string |  |

## Native endpoint

Through the native Alto API, this operation is `GET /inventory` (base URL `https://api.alto.zoopladev.co.uk`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-inventory.md) for the provider-specific parameters and requirements.

