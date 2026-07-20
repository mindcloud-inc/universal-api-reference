# Lettr: Verify Domain



```
PUT https://connect.mindcloud.co/v1/universal/lettr/latest/actions/verify-domain
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lettr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/lettr/latest/actions/verify-domain" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lettr/latest/actions/verify-domain', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `domain` | string | yes | Sending domain name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "cname_status": "Ava Chen",
        "cname_warning_level": 1,
        "dkim_status": "string",
        "dkim_warning_level": 1,
        "dmarc": {
          "covered_by_parent_policy": true,
          "error": "string",
          "found_at_domain": "string",
          "is_valid": true,
          "policy": "string",
          "record": "string",
          "status": "string",
          "subdomain_policy": "string"
        },
        "dmarc_status": "string",
        "dmarc_warning_level": 1,
        "dns": {
          "cname_error": "Ava Chen",
          "cname_record": "Ava Chen",
          "dkim_error": "string",
          "dkim_record": "string",
          "dmarc_error": "string",
          "dmarc_record": "string",
          "spf_error": "string",
          "spf_record": "string"
        },
        "domain": "string",
        "is_primary_domain": true,
        "ownership_verified": true,
        "spf_status": "string",
        "spf_warning_level": 1
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Domain verification payload. |
| `data.cname_status` | string | CNAME verification status. |
| `data.cname_warning_level` | number | CNAME warning level. |
| `data.dkim_status` | string | DKIM verification status. |
| `data.dkim_warning_level` | number | DKIM warning level. |
| `data.dmarc` | object | Parsed DMARC evaluation. |
| `data.dmarc_status` | string | DMARC verification status. |
| `data.dmarc_warning_level` | number | DMARC warning level. |
| `data.dmarc.covered_by_parent_policy` | boolean | Whether the domain inherits a parent DMARC policy. |
| `data.dmarc.error` | string | DMARC parsing error when present. |
| `data.dmarc.found_at_domain` | string | Domain where the DMARC record was found. |
| `data.dmarc.is_valid` | boolean | Whether the DMARC policy is valid. |
| `data.dmarc.policy` | string | DMARC policy value. |
| `data.dmarc.record` | string | Raw DMARC record. |
| `data.dmarc.status` | string | DMARC validation status. |
| `data.dmarc.subdomain_policy` | string | DMARC subdomain policy value. |
| `data.dns` | object | DNS verification details. |
| `data.dns.cname_error` | string | CNAME verification error when present. |
| `data.dns.cname_record` | string | Observed CNAME record. |
| `data.dns.dkim_error` | string | DKIM verification error when present. |
| `data.dns.dkim_record` | string | Observed DKIM record. |
| `data.dns.dmarc_error` | string | DMARC verification error when present. |
| `data.dns.dmarc_record` | string | Observed DMARC record. |
| `data.dns.spf_error` | string | SPF verification error when present. |
| `data.dns.spf_record` | string | Observed SPF record. |
| `data.domain` | string | Sending domain name. |
| `data.is_primary_domain` | boolean | Whether this is the primary domain. |
| `data.ownership_verified` | boolean | Whether ownership is verified when Lettr reports it. |
| `data.spf_status` | string | SPF verification status. |
| `data.spf_warning_level` | number | SPF warning level. |
| `message` | string | Domain verification status message. |

## Native endpoint

Through the native Lettr API, this operation is `POST /domains/:domain/verify` (base URL `https://app.lettr.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-domain.md) for the provider-specific parameters and requirements.

