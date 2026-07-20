# DMARC Report: Update Domain

Updates an existing domain in DMARC Report.

```
PUT https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/update-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/update-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "id": "string",
  "domain": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/update-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "id": "string",
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
| `id` | string | yes | Domain identifier from the endpoint path. |
| `domain` | object | yes | Domain update hash. Supported keys include rua_report, ruf_report, mta_sts_report, hosted_dmarc, hosted_dmarc_config, and hosted_mta_sts. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
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
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Domain address. |
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

## Native endpoint

Through the native DMARC Report API, this operation is `PUT /accounts/:accountId/domains/:id.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-domain.md) for the provider-specific parameters and requirements.

