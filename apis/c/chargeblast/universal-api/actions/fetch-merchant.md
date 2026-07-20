# Chargeblast: Fetch Merchant

Retrieves a merchant from Chargeblast.

```
GET https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-merchant
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chargeblast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-merchant?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/chargeblast/latest/actions/fetch-merchant?${params}`, {
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
| `merchantId` | string | no | The merchant ID to fetch. Chargeblast documents this query parameter as optional. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientId": "string",
      "id": "string",
      "merchant_id": "string",
      "name": "Ava Chen",
      "rcode": "string",
      "sites": [
        {}
      ],
      "source": "string",
      "user": {},
      "verifi_name": "Ava Chen",
      "verifiRiskLevel": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientId` | string | The client ID returned by Chargeblast when present. |
| `id` | string | The Chargeblast merchant record ID. |
| `merchant_id` | string | The provider-facing merchant identifier returned by Chargeblast. |
| `name` | string | The merchant display name. |
| `rcode` | string | The retailer code returned by Chargeblast. |
| `sites` | array<object> | The merchant sites returned by Chargeblast. |
| `source` | string | The enrollment source returned by Chargeblast. |
| `user` | object | The user object associated with the merchant. |
| `verifi_name` | string | The Verifi merchant name when present. |
| `verifiRiskLevel` | string | The Verifi risk level when present. |

## Native endpoint

Through the native Chargeblast API, this operation is `GET /api/merchant` (base URL `https://api.chargeblast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-merchant.md) for the provider-specific parameters and requirements.

