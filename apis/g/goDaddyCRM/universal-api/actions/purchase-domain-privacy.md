# GoDaddy CRM: Purchase Domain Privacy

Purchases domain privacy for a GoDaddy domain.

```
POST https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/purchase-domain-privacy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoDaddy CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/purchase-domain-privacy" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "example.com",
  "consent.agreementKeys[]": "DNPA",
  "consent.agreedBy": "203.0.113.10",
  "consent.agreedAt": "2026-03-26T17:30:00Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goDaddyCRM/latest/actions/purchase-domain-privacy', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "example.com",
    "consent.agreementKeys[]": "DNPA",
    "consent.agreedBy": "203.0.113.10",
    "consent.agreedAt": "2026-03-26T17:30:00Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | Required domain for the privacy purchase Example: `example.com`. |
| `consent.agreementKeys[]` | string<string> | yes | Required agreement keys, including DNPA Accepts multiple values as an array. Example: `DNPA`. |
| `consent.agreedBy` | string | yes | Required IP address of the consenting end user Example: `203.0.113.10`. |
| `consent.agreedAt` | string | yes | Required consent timestamp in ISO format Example: `2026-03-26T17:30:00Z`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoDaddy CRM API returns.

## Native endpoint

Through the native GoDaddy CRM API, this operation is `POST /v1/domains/:domain/privacy/purchase` (base URL `https://api.godaddy.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/purchase-domain-privacy.md) for the provider-specific parameters and requirements.

