# GoDaddy CRM: Validate Domain Transfer

Validates a domain transfer in GoDaddy.

```
POST https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/validate-domain-transfer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/validate-domain-transfer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "domain": "string",
  "authCode": "string",
  "consent": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/validate-domain-transfer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "domain": "string",
    "authCode": "string",
    "consent": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes | The Customer identifier. Use the shopper ID unless you are operating on behalf of a reseller subaccount. |
| `domain` | string | yes | The domain name to transfer in. |
| `authCode` | string | yes | The authorization code for the transfer-in domain. |
| `consent` | object | yes | Consent details including agreedAt, agreedBy, and agreementKeys. |
| `renewAuto` | boolean | no | Whether the domain should automatically renew after transfer. |
| `privacy` | boolean | no | Whether privacy should be enabled. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `period` | number | no | Transfer renewal period in years. |
| `identityDocumentId` | string | no | Identity document identifier when required by the transfer schema. |
| `contacts` | object | no | Registrant and related contact objects when required by the transfer schema. |
| `metadata` | object | no | Additional metadata supported by the transfer schema. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `POST /v2/customers/:customerId/domains/:domain/transfer/validate` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-domain-transfer.md) for the provider-specific parameters and requirements.

