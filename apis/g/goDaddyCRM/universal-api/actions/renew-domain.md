# GoDaddy CRM: Renew Domain

Renews a domain in your GoDaddy account.

```
POST https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/renew-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/renew-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "domain": "string",
  "expires": "2026-05-07T12:00:00.000Z",
  "consent": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/renew-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "domain": "string",
    "expires": "2026-05-07T12:00:00.000Z",
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
| `domain` | string | yes | The domain name to renew. |
| `expires` | date | yes | The resulting expiration timestamp for the renewed domain. |
| `consent` | object | yes | Consent details including agreedAt, agreedBy, and agreementKeys. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `period` | number | no | Renewal period in years. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `POST /v2/customers/:customerId/domains/:domain/renew` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/renew-domain.md) for the provider-specific parameters and requirements.

