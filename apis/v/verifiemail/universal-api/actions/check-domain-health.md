# verifi.email: Check Domain Health

Check a domain's email-authentication health and return SPF, DKIM, DMARC, and BIMI scores with recommendations.

```
GET https://connect.mindcloud.co/v1/universal/verifiemail/latest/actions/check-domain-health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a verifi.email `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/verifiemail/latest/actions/check-domain-health?connectionId=$CONNECTION_ID&domain=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "domain": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/verifiemail/latest/actions/check-domain-health?${params}`, {
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
| `domain` | string | yes | Domain to inspect. |
| `selector` | string | no | Optional DKIM selector to test directly. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bimi": {
        "exists": true,
        "recommendation": "string",
        "records": [
          "string"
        ],
        "score": 1,
        "target_score": 1
      },
      "dkim": {
        "exists": true,
        "recommendation": "string",
        "records": [
          "string"
        ],
        "score": 1,
        "target_score": 1
      },
      "dmarc": {
        "exists": true,
        "policy": "string",
        "recommendation": "string",
        "records": [
          "string"
        ],
        "score": 1,
        "target_score": 1
      },
      "domain": "string",
      "score": 1,
      "spf": {
        "exists": true,
        "policy": "string",
        "recommendation": "string",
        "records": [
          "string"
        ],
        "score": 1,
        "target_score": 1
      },
      "target_score": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bimi.exists` | boolean | Whether a BIMI record exists. |
| `bimi.recommendation` | string | Improvement guidance for BIMI. |
| `bimi.records` | array<string> | Published BIMI records. |
| `bimi.score` | number | Current BIMI score. |
| `bimi.target_score` | number | Recommended BIMI target score. |
| `dkim.exists` | boolean | Whether a DKIM record exists for the selector. |
| `dkim.recommendation` | string | Improvement guidance for DKIM. |
| `dkim.records` | array<string> | Published DKIM records. |
| `dkim.score` | number | Current DKIM score. |
| `dkim.target_score` | number | Recommended DKIM target score. |
| `dmarc.exists` | boolean | Whether a DMARC record exists. |
| `dmarc.policy` | string | Observed DMARC enforcement policy. |
| `dmarc.recommendation` | string | Improvement guidance for DMARC. |
| `dmarc.records` | array<string> | Published DMARC records. |
| `dmarc.score` | number | Current DMARC score. |
| `dmarc.target_score` | number | Recommended DMARC target score. |
| `domain` | string | Domain that was inspected. |
| `score` | number | Overall domain health score. |
| `spf.exists` | boolean | Whether an SPF record exists. |
| `spf.policy` | string | Observed SPF enforcement policy. |
| `spf.recommendation` | string | Improvement guidance for SPF. |
| `spf.records` | array<string> | Published SPF records. |
| `spf.score` | number | Current SPF score. |
| `spf.target_score` | number | Recommended SPF target score. |
| `target_score` | number | Recommended overall target score. |

## Native endpoint

Through the native verifi.email API, this operation is `GET /v1/domain/check` (base URL `https://api.verifi.email`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-domain-health.md) for the provider-specific parameters and requirements.

