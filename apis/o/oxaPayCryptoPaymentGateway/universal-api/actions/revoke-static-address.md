# OxaPay Crypto Payment Gateway: Revoke Static Address

Deletes an existing static address from OxaPay.

```
DELETE https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/revoke-static-address
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OxaPay Crypto Payment Gateway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/revoke-static-address?connectionId=$CONNECTION_ID&address=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/revoke-static-address?${params}`, {
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
| `address` | string | yes | Static address to revoke. |
| `network` | string | no | Blockchain network of the static address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "error": {},
      "message": "string",
      "status": 1,
      "version": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Revocation response payload. |
| `error` | object | Provider error payload when present. |
| `message` | string | Provider message. |
| `status` | number | HTTP-style status code. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native OxaPay Crypto Payment Gateway API, this operation is `POST /payment/static-address/revoke` (base URL `https://api.oxapay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/revoke-static-address.md) for the provider-specific parameters and requirements.

