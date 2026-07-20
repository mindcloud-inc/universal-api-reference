# OxaPay Crypto Payment Gateway: Get System Status

Retrieves system status from OxaPay.

```
GET https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/get-system-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OxaPay Crypto Payment Gateway `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/get-system-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oxaPayCryptoPaymentGateway/latest/actions/get-system-status?${params}`, {
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
      "data": {
        "status": "string"
      },
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
| `data` | object | Status payload. |
| `data.status` | string | Current API status. |
| `error` | object | Provider error payload when present. |
| `message` | string | Provider message. |
| `status` | number | HTTP-style status code. |
| `version` | string | Provider API version. |

## Native endpoint

Through the native OxaPay Crypto Payment Gateway API, this operation is `GET /common/monitor` (base URL `https://api.oxapay.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-system-status.md) for the provider-specific parameters and requirements.

