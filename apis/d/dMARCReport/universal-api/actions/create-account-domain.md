# DMARC Report: Create Account Domain

Creates a domain account in DMARC Report.

```
POST https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/create-account-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/create-account-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "domain_account": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/create-account-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "domain_account": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | DMARC Report account identifier from the endpoint path. |
| `domain_account` | object | yes | Domain account payload hash. Include account_attributes with id and domain_ids. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": 1,
      "domainId": 1,
      "id": 1,
      "timestamp": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | number | Account identifier linked to the domain. |
| `domainId` | number | Domain identifier linked to the account. |
| `id` | number | Account-domain relationship identifier. |
| `timestamp` | date | Relationship timestamp when returned. |

## Native endpoint

Through the native DMARC Report API, this operation is `POST /accounts/:accountId/domain_accounts.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-account-domain.md) for the provider-specific parameters and requirements.

