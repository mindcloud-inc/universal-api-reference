# Ship&Co: List Shipments



```
GET https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/list-shipments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/list-shipments?${params}`, {
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
| `carrier` | string | no | Optional carrier type filter. |
| `scope` | string | no | Shipment scope: api or all. |
| `state` | string | no | Shipment state: active, void, or any. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `created_after` | date | no | Only include shipments created after this ISO timestamp. |
| `created_before` | date | no | Only include shipments created before this ISO timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "delivery": {},
      "from_address": {},
      "id": "string",
      "state": "string",
      "to_address": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Shipment creation timestamp. |
| `delivery` | object | Carrier, tracking number, label, and invoice details. |
| `from_address` | object | Sender address. |
| `id` | string | Shipment ID. |
| `state` | string | Shipment state. |
| `to_address` | object | Recipient address. |

## Native endpoint

Through the native Ship&Co API, this operation is `GET /shipments` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-shipments.md) for the provider-specific parameters and requirements.

