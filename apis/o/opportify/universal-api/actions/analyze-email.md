# Opportify: Analyze Email

Analyzes an email address in Opportify for deliverability and risk.

```
GET https://connect.mindcloud.co/v1/universal/opportify/latest/actions/analyze-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Opportify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/analyze-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/opportify/latest/actions/analyze-email?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | The email address to validate. |
| `enableAI` | boolean | no | Enable AI-driven risk analysis. Optional; defaults to `true`. |
| `enableAutoCorrection` | boolean | no | Controls email auto-correction behavior. Default: `false`. - When set to `true`: If the system is highly confident about a correction, it will automatically apply it. The analysis will be performed on the corrected email address. The response will include the corrected email in `emailAddress` and `emailCorrection`, with the original input preserved in `emailAutoCorrectedFrom`. - When set to `false`: The system will still identify and return potential corrections in the `emailCorrection` field when confident, but the analysis will remain based on the original email address provided in the input. The `emailAutoCorrectedFrom` field will not be present. |
| `enableDomainEnrichment` | boolean | no | Include domain-level enrichment details. Optional; defaults to `true`. Set to `false` to omit the `domain` block even when the data exists. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addressSignals": {},
      "domain": {},
      "emailAddress": "ava@example.com",
      "emailAutoCorrectedFrom": "ava@example.com",
      "emailCorrection": "ava@example.com",
      "emailDNS": {},
      "emailProvider": "ava@example.com",
      "emailType": "ava@example.com",
      "isCatchAll": true,
      "isDeliverable": "string",
      "isFormatValid": true,
      "isMailboxFull": true,
      "isReachable": true,
      "riskReport": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addressSignals` | object | Local-part parsing details for the analyzed address. Always present; fields default to empty strings when a signal is not applicable. |
| `domain` | object | Domain summary derived from enrichment providers. Omitted when enrichment is unavailable or `enableDomainEnrichment` is set to `false`. |
| `emailAddress` | string | Normalized email address returned by the service (always lower-case). |
| `emailAutoCorrectedFrom` | string | The original email address provided in the request, before auto-correction was applied. This field is only present when `enableAutoCorrection` is `true` AND the system automatically applied a correction.  When this field is present, it indicates that: - The user submitted this email address - The system detected a confident correction - `emailAddress` contains the corrected value used for analysis - `emailCorrection` contains the same corrected value |
| `emailCorrection` | string | The corrected email address when the system is highly confident about a typo or misspelling. Always present; empty string when no correction is needed.  - When `enableAutoCorrection` is `true` and correction applied: Contains the corrected email (same as `emailAddress`). The original input is available in `emailAutoCorrectedFrom`. - When `enableAutoCorrection` is `false`: Contains the suggested correction, but `emailAddress` and all analysis remain based on the original input. - When no correction is needed: Empty string. |
| `emailDNS` | object | DNS details for an email address domain. |
| `emailProvider` | string | Provider slug derived from the domain, or `unknown` when not classified. |
| `emailType` | string | Email classification based on provider and enrichment signals. Allowed values: `private`, `free`, `disposable`, `unknown`. Example: `free`. |
| `isCatchAll` | boolean | Determines if the email domain is configured as a catch-all, which accepts emails for all addresses within the domain. This is verified through multiple email tests. |
| `isDeliverable` | string | Checks if the email address exists and is deliverable using SMTP handshake simulation. This involves connecting to the mail server and issuing commands to verify deliverability. The possible answers are `yes`, `no`, or `unknown`. We guarantee a high confidence level on this parameter since this is a real time verification. Allowed values: `yes`, `no`, `unknown`. Example: `yes`. |
| `isFormatValid` | boolean | Indicates if the email address meets syntax validation rules. |
| `isMailboxFull` | boolean | Determines if the mailbox associated with the email is full, in association with isDeliverable field, it can give a reason why the email is not deliverable. |
| `isReachable` | boolean | Confirms if the email domain has valid MX DNS records using DNS lookup. |
| `riskReport` | object | AI-generated risk report detailing the evaluated risk bucket. Returned only when `enableAI` is true. |

## Native endpoint

Through the native Opportify API, this operation is `POST /email/analyze` (base URL `https://api.opportify.ai/insights/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/analyze-email.md) for the provider-specific parameters and requirements.

