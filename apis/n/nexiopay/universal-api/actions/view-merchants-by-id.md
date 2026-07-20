# Nexiopay: View merchants by ID



```
GET https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-merchants-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nexiopay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-merchants-by-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nexiopay/latest/actions/view-merchants-by-id?${params}`, {
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
| `merchantIds` | string | no | Comma-separated Nexio merchant IDs to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currencyId": "string",
      "hasAuthorizeNetApmCreds": true,
      "isApmConfigured": true,
      "isPaymentConfigured": true,
      "isPaymentRecoveryConfigured": true,
      "kount": {},
      "kountMerc": "string",
      "merchantId": "string",
      "name": "Ava Chen",
      "processor": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Merchant creation timestamp. |
| `currencyId` | string | Merchant currency identifier. |
| `hasAuthorizeNetApmCreds` | boolean | Whether Authorize.Net APM credentials are present. |
| `isApmConfigured` | boolean | Whether alternative payment methods are configured. |
| `isPaymentConfigured` | boolean | Whether payment processing is configured. |
| `isPaymentRecoveryConfigured` | boolean | Whether payment recovery is configured. |
| `kount` | object | Kount configuration object. |
| `kountMerc` | string | Kount merchant identifier. |
| `merchantId` | string | Nexio merchant ID. |
| `name` | string | Merchant name. |
| `processor` | object | Processor metadata when returned. |
| `updatedAt` | date | Merchant last update timestamp. |

## Native endpoint

Through the native Nexiopay API, this operation is `GET /merchant/v3` (base URL `https://api.nexiopaysandbox.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-merchants-by-id.md) for the provider-specific parameters and requirements.

