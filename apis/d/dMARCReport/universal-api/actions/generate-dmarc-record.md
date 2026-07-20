# DMARC Report: Generate DMARC Record

Generates a DMARC record for a domain in DMARC Report.

```
POST https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/generate-dmarc-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DMARC Report `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/generate-dmarc-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string",
  "domainId": "string",
  "p": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dMARCReport/latest/actions/generate-dmarc-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string",
    "domainId": "string",
    "p": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | DMARC Report account identifier from the endpoint path. |
| `domainId` | string | yes | Domain identifier from the endpoint path. |
| `p` | string | yes | DMARC policy to generate in the record. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sp` | string | no | Optional DMARC policy for subdomains. |
| `pct` | number | no | Percentage of messages to which the DMARC policy applies. |
| `adkim` | string | no | DKIM alignment mode: relaxed or strict. |
| `aspf` | string | no | SPF alignment mode: relaxed or strict. |
| `fo` | string | no | DMARC forensic reporting options, such as 0, 1, d, s, or a colon-separated combination. |
| `additionalRuaEmails[]` | array<string> | no | Additional email addresses for aggregate reports. Accepts multiple values as an array. |
| `additionalRufEmails[]` | array<string> | no | Additional email addresses for forensic reports. Accepts multiple values as an array. |
| `t` | string | no | DMARCbis test mode value: y or n. |
| `psd` | string | no | DMARCbis public suffix domain value: y, n, or u. |
| `np` | string | no | DMARCbis policy for non-existent subdomains. |
| `publish` | boolean | no | Whether to publish this generated record to hosted DMARC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dmarcRecord": "string",
      "maxLength": 1,
      "recordLength": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dmarcRecord` | string | Generated DMARC TXT record value. |
| `maxLength` | number | Maximum allowed record length. |
| `recordLength` | number | Length of the generated record. |

## Native endpoint

Through the native DMARC Report API, this operation is `POST /accounts/:accountId/domains/:domainId/generate_dmarc_record.json` (base URL `https://api.dmarcreport.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-dmarc-record.md) for the provider-specific parameters and requirements.

