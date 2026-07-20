# Mercado Pago: Get Claim Details

Retrieves claim details from Mercado Pago.

```
GET https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/get-claim-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mercado Pago `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/get-claim-details?connectionId=$CONNECTION_ID&claim_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "claim_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mercadoPago/latest/actions/get-claim-details?${params}`, {
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
| `claim_id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Mercado Pago API, this operation is `GET /post-purchase/v1/claims/{claim_id}` (base URL `https://api.mercadopago.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-claim-details.md) for the provider-specific parameters and requirements.

