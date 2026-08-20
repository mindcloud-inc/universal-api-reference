# Centerpoint: List Production Purchase Orders



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-production-purchase-orders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-production-purchase-orders?connectionId=$CONNECTION_ID&limit=25&offset=0&PRODUCTION_ID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "PRODUCTION_ID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/list-production-purchase-orders?${params}`, {
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
| `PRODUCTION_ID` | string | yes | The production id to retrieve. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields[profiles]` | string | no | Optional fields profiles query parameter. |
| `fields[employees]` | string | no | Optional fields employees query parameter. |
| `include` | string | no | Optional include query parameter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "approvedAt": "string",
        "createdAt": "string",
        "deletedAt": {},
        "description": {},
        "externalId": "string",
        "name": "Ava Chen",
        "price": 1,
        "type": "string",
        "updatedAt": "string",
        "workDate": "string"
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.approvedAt` | string |  |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.description` | object |  |
| `attributes.externalId` | string |  |
| `attributes.name` | string |  |
| `attributes.price` | number |  |
| `attributes.type` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.workDate` | string |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET productions/:PRODUCTION_ID/purchase_orders` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-production-purchase-orders.md) for the provider-specific parameters and requirements.

