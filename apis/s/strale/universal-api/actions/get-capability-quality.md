# Strale: Get Capability Quality

Retrieves a capability quality score from Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-capability-quality
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-capability-quality?connectionId=$CONNECTION_ID&slug=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "slug": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/get-capability-quality?${params}`, {
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
| `slug` | string | yes | Capability slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "capability": "string",
      "pending": true,
      "qualityProfile": {
        "grade": "string",
        "label": "string",
        "score": 1
      },
      "reliabilityProfile": {
        "capabilityType": "string",
        "grade": "string",
        "label": "string",
        "score": 1
      },
      "runsAnalyzed": 1,
      "sqs": {
        "freshnessLevel": "string",
        "label": "string",
        "rawScore": 1,
        "score": 1,
        "trend": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `capability` | string | Capability slug covered by this quality report. |
| `pending` | boolean | Whether quality data is still pending. |
| `qualityProfile.grade` | string | Overall quality grade. |
| `qualityProfile.label` | string | Human-readable quality label. |
| `qualityProfile.score` | number | Overall quality score. |
| `reliabilityProfile.capabilityType` | string | Provider reliability model classification. |
| `reliabilityProfile.grade` | string | Overall reliability grade. |
| `reliabilityProfile.label` | string | Human-readable reliability label. |
| `reliabilityProfile.score` | number | Overall reliability score. |
| `runsAnalyzed` | number | Number of historical runs included in this report. |
| `sqs.freshnessLevel` | string | Freshness indicator for recent tests. |
| `sqs.label` | string | Human-readable SQS label. |
| `sqs.rawScore` | number | Underlying unrounded Strale quality score. |
| `sqs.score` | number | Current Strale quality score. |
| `sqs.trend` | string | Current score trend. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/quality/:slug` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-capability-quality.md) for the provider-specific parameters and requirements.

