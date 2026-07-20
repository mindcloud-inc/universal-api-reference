# GoDaddy CRM: Validate Domain Registration

Validates a domain registration in GoDaddy.

```
POST https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/validate-domain-registration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/validate-domain-registration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "domain": "string",
  "consent": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/validate-domain-registration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "domain": "string",
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
| `domain` | string | yes | The domain name to validate for registration. |
| `consent` | object | yes | Consent details including agreedAt, agreedBy, and agreementKeys. |
| `renewAuto` | boolean | no | Whether the domain should automatically renew. |
| `privacy` | boolean | no | Whether privacy should be enabled. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `period` | number | no | Registration period in years. |
| `nameServers[]` | array<string> | no | Custom name servers for the domain. |
| `contacts` | object | no | Registrant and related contact objects when required by the TLD schema. |
| `metadata` | object | no | Additional metadata supported by the registration schema. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `POST /v2/customers/:customerId/domains/register/validate` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-domain-registration.md) for the provider-specific parameters and requirements.

