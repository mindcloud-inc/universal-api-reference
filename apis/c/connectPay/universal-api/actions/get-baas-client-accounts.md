# ConnectPay: Get BaaS Client Accounts

Retrieves a BaaS client's accounts from ConnectPay.

```
GET https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-baas-client-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ConnectPay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-baas-client-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/connectPay/latest/actions/get-baas-client-accounts?${params}`, {
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
| `baasClientId` | string | no | BaaS client ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ConnectPay API returns.

## Native endpoint

Through the native ConnectPay API, this operation is `GET /ob/baas/clients/:baasClientId/accounts` (base URL `https://api-stage.connectpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-baas-client-accounts.md) for the provider-specific parameters and requirements.

