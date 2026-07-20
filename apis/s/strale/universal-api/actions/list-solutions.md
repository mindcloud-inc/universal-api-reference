# Strale: List Solutions

Retrieves solutions from Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-solutions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-solutions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-solutions?${params}`, {
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
| `category` | string | no | Filter by solution category slug. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "description": "string",
      "freshnessLevel": "string",
      "geography": "string",
      "lastTestedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "priceCents": 1,
      "quality": "string",
      "reliability": "string",
      "slug": "string",
      "sqs": 1,
      "sqsLabel": "string",
      "stepCount": 1,
      "strategy": "string",
      "transparencyTag": "string",
      "trend": "string",
      "usable": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `category` | string | Solution category. |
| `description` | string | Solution description. |
| `freshnessLevel` | string | Freshness indicator. |
| `geography` | string | Geography scope. |
| `lastTestedAt` | date | Most recent test timestamp. |
| `name` | string | Solution name. |
| `priceCents` | number | Solution price in cents. |
| `quality` | string | Quality grade. |
| `reliability` | string | Reliability grade. |
| `slug` | string | Solution slug. |
| `sqs` | number | Strale quality score. |
| `sqsLabel` | string | Human-readable quality label. |
| `stepCount` | number | Number of steps in the solution. |
| `strategy` | string | Execution strategy. |
| `transparencyTag` | string | Transparency classification. |
| `trend` | string | Current trend label. |
| `usable` | boolean | Whether the solution is currently usable. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/solutions` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-solutions.md) for the provider-specific parameters and requirements.

