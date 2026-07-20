# Strale: List Capabilities

Retrieves capabilities from Strale.

```
GET https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-capabilities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Strale `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-capabilities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/strale/latest/actions/list-capabilities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "dataSource": "string",
      "description": "string",
      "freshnessLevel": "string",
      "geography": "string",
      "isFreeTier": true,
      "lastTestedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "priceCents": 1,
      "quality": "string",
      "reliability": "string",
      "slug": "string",
      "sqs": 1,
      "sqsLabel": "string",
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
| `category` | string | Capability category. |
| `dataSource` | string | Primary data source description. |
| `description` | string | Capability description. |
| `freshnessLevel` | string | Freshness indicator. |
| `geography` | string | Geography scope. |
| `isFreeTier` | boolean | Whether the capability is available in a free tier. |
| `lastTestedAt` | date | Most recent test timestamp. |
| `name` | string | Capability name. |
| `priceCents` | number | Capability price in cents. |
| `quality` | string | Quality grade. |
| `reliability` | string | Reliability grade. |
| `slug` | string | Capability slug. |
| `sqs` | number | Strale quality score. |
| `sqsLabel` | string | Human-readable quality label. |
| `strategy` | string | Execution strategy. |
| `transparencyTag` | string | Transparency classification. |
| `trend` | string | Current trend label. |
| `usable` | boolean | Whether the capability is currently usable. |

## Native endpoint

Through the native Strale API, this operation is `GET /v1/capabilities` (base URL `https://api.strale.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-capabilities.md) for the provider-specific parameters and requirements.

