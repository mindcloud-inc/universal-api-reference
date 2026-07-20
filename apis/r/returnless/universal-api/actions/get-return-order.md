# Returnless: Get Return Order

Retrieves a return order from Returnless.

```
GET https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-return-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Returnless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-return-order?connectionId=$CONNECTION_ID&returnOrder=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "returnOrder": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/returnless/latest/actions/get-return-order?${params}`, {
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
| `returnOrder` | string | yes | The unique identifier of the return order. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Return order payload retrieved by ID. |
| `meta` | object | Execution metadata. |

## Native endpoint

Through the native Returnless API, this operation is `GET /2025-01/return-orders/{returnOrder}` (base URL `https://api-v2.returnless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-return-order.md) for the provider-specific parameters and requirements.

