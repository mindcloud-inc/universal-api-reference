# DMARC Report: Create Domain

Creates a domain in a DMARC Report account.

```
POST https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/create-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/create-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "domain": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/create-domain', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "domain": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | DMARC Report account identifier from the endpoint path. |
| `domain` | object | yes | Domain attributes hash. Include address, rua_report, and ruf_report; at least one report flag must be true. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dmarcStatus": "string",
      "hostedDmarc": true,
      "hostedMtaSts": true,
      "id": 1,
      "mtaStsReport": true,
      "mtaStsStatus": "string",
      "parkedDomain": true,
      "ruaReport": true,
      "rufReport": true,
      "slug": "string",
      "tags": [
        {}
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Domain address. |
| `createdAt` | date | Domain creation timestamp. |
| `dmarcStatus` | string | DMARC status for the domain. |
| `hostedDmarc` | boolean | Whether hosted DMARC is enabled. |
| `hostedMtaSts` | boolean | Whether hosted MTA-STS is enabled. |
| `id` | number | Domain identifier. |
| `mtaStsReport` | boolean | Whether MTA-STS reporting is enabled. |
| `mtaStsStatus` | string | MTA-STS status for the domain. |
| `parkedDomain` | boolean | Whether the domain is parked. |
| `ruaReport` | boolean | Whether RUA aggregate reports are enabled. |
| `rufReport` | boolean | Whether RUF forensic reports are enabled. |
| `slug` | string | Domain slug. |
| `tags` | array<object> | Tag objects associated with the domain. |
| `updatedAt` | date | Domain update timestamp. |
| `userId` | number | Owner user identifier. |

## Native endpoint

Through the native DMARC Report API, this operation is `POST /accounts/:accountId/domains.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-domain.md) for the provider-specific parameters and requirements.

