# Sumo Logic: List Transformation Rules

Retrieves transformation rules from your Sumo Logic organization.

```
GET https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-transformation-rules
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sumo Logic `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-transformation-rules?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sumoLogic/latest/actions/list-transformation-rules?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "enabled": true,
      "id": "string",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "modifiedBy": "string",
      "ruleDefinition": {
        "dimensionTransformations": [
          {
            "transformationType": "string"
          }
        ],
        "name": "Ava Chen",
        "retention": 1,
        "selector": "string",
        "transformedMetricsRetention": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy` | string |  |
| `enabled` | boolean |  |
| `id` | string |  |
| `modifiedAt` | date |  |
| `modifiedBy` | string |  |
| `ruleDefinition.dimensionTransformations[].transformationType` | string |  |
| `ruleDefinition.name` | string |  |
| `ruleDefinition.retention` | number |  |
| `ruleDefinition.selector` | string |  |
| `ruleDefinition.transformedMetricsRetention` | number |  |

## Native endpoint

Through the native Sumo Logic API, this operation is `GET /v1/transformationRules` (base URL `https://api.sumologic.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-transformation-rules.md) for the provider-specific parameters and requirements.

