# Mailcheck: Verify Email Authenticity



```
POST https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/verify-email-authenticity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/verify-email-authenticity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "headers": "From: sender@example.com\nReceived: from ..."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/verify-email-authenticity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "headers": "From: sender@example.com\nReceived: from ..."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `headers` | string | yes | Raw email header block to analyze for authenticity. Example: `From: sender@example.com Received: from ...`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trustedDomains[]` | array<string> | no | Optional list of trusted domains used for lookalike detection. Provide a JSON array of domain strings. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "anomalies": [
        [
          {}
        ]
      ],
      "authentication": {
        "dkim": {
          "has_public_key": true,
          "result": "string"
        },
        "dmarc": {
          "has_policy": true,
          "policy": "string",
          "record": "string"
        },
        "spf": {
          "domain": "string",
          "result": "string"
        }
      },
      "credits_remaining": 1,
      "from": {
        "address": "string",
        "display_name": "Ava Chen",
        "domain": "string"
      },
      "lookalike": {
        "is_lookalike": true
      },
      "privacy": {
        "body_processed": true,
        "headers_only": true
      },
      "trust_score": 1,
      "verdict": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anomalies[]` | array<object> | Detected anomalies. |
| `authentication` | object | Authentication check results. |
| `authentication.dkim` | object | DKIM analysis. |
| `authentication.dkim.has_public_key` | boolean | Whether the DKIM public key exists. |
| `authentication.dkim.result` | string | DKIM result. |
| `authentication.dmarc` | object | DMARC analysis. |
| `authentication.dmarc.has_policy` | boolean | Whether a DMARC policy exists. |
| `authentication.dmarc.policy` | string | DMARC enforcement policy. |
| `authentication.dmarc.record` | string | Observed DMARC record or evidence. |
| `authentication.spf` | object | SPF analysis. |
| `authentication.spf.domain` | string | SPF-authenticated domain when available. |
| `authentication.spf.result` | string | SPF result. |
| `credits_remaining` | number | Remaining monthly credits after the analysis. |
| `from` | object | Parsed sender identity. |
| `from.address` | string | Sender email address. |
| `from.display_name` | string | Sender display name. |
| `from.domain` | string | Sender domain. |
| `lookalike` | object | Lookalike-domain detection result. |
| `lookalike.is_lookalike` | boolean | Whether the sender domain resembles a trusted domain. |
| `privacy` | object | Privacy guarantees for processing. |
| `privacy.body_processed` | boolean | Whether the body was processed. |
| `privacy.headers_only` | boolean | Whether only headers were analyzed. |
| `trust_score` | number | Overall trust score from 0 to 100. |
| `verdict` | string | Overall authenticity verdict. |

## Native endpoint

Through the native Mailcheck API, this operation is `POST /v1/verify/auth` (base URL `https://api.mailcheck.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/verify-email-authenticity.md) for the provider-specific parameters and requirements.

