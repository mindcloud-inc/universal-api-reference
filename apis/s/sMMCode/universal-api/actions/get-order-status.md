# SMMCode: Get Order Status



```
GET https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/get-order-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SMMCode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/get-order-status?connectionId=$CONNECTION_ID&order=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "order": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sMMCode/latest/actions/get-order-status?${params}`, {
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
| `order` | string | yes | Order ID to check. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "charge": "string",
      "currency": "string",
      "remains": "string",
      "start_count": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `charge` | string | Order charge. |
| `currency` | string | Charge currency. |
| `remains` | string | Remaining quantity. |
| `start_count` | string | Starting count for the order. |
| `status` | string | Order status. |

## Native endpoint

Through the native SMMCode API, this operation is `POST /api/v2` (base URL `https://extended.smmcode.org`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-order-status.md) for the provider-specific parameters and requirements.

