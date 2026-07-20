# Strale: Suggest Capability

Suggests capabilities or solutions in Strale for a query.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/suggest-capability
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/suggest-capability?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/suggest-capability?${params}`, {
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
| `limit` | number | no | Maximum number of suggestions to return. |
| `query` | string | yes | Natural language query for capability or solution suggestions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "queryUnderstoodAs": "string",
      "recommendation": {
        "badge": "string",
        "description": "string",
        "geography": "string",
        "matchReason": "string",
        "name": "Ava Chen",
        "priceCents": 1,
        "slug": "string",
        "stepCount": 1,
        "trust": {
          "badge": "string",
          "badgeLabel": "string",
          "dataSource": "string",
          "lastTestedAt": "2026-05-07T12:00:00.000Z",
          "sqs": 1,
          "sqsLabel": "string",
          "testsPassing": 1,
          "testsTotal": 1
        },
        "type": "string"
      },
      "totalMatches": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `queryUnderstoodAs` | string | Provider interpretation of the input query. |
| `recommendation.badge` | string | Provider trust badge. |
| `recommendation.description` | string | Recommended result description. |
| `recommendation.geography` | string | Geography scope for the recommendation. |
| `recommendation.matchReason` | string | Why the recommendation matches the query. |
| `recommendation.name` | string | Recommended capability or solution name. |
| `recommendation.priceCents` | number | Estimated price in cents. |
| `recommendation.slug` | string | Recommended capability or solution slug. |
| `recommendation.stepCount` | number | Number of execution steps in the recommendation. |
| `recommendation.trust.badge` | string | Trust badge identifier. |
| `recommendation.trust.badgeLabel` | string | Trust badge label. |
| `recommendation.trust.dataSource` | string | Quality data source. |
| `recommendation.trust.lastTestedAt` | date | Most recent automated test timestamp. |
| `recommendation.trust.sqs` | number | Strale quality score for the recommendation. |
| `recommendation.trust.sqsLabel` | string | Human-readable SQS label. |
| `recommendation.trust.testsPassing` | number | Passing automated tests. |
| `recommendation.trust.testsTotal` | number | Total automated tests. |
| `recommendation.type` | string | Recommended result type. |
| `totalMatches` | number | Total number of matches found for the query. |

## Native endpoint

Through the native Strale API, this operation is `POST /v1/suggest` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/suggest-capability.md) for the provider-specific parameters and requirements.

