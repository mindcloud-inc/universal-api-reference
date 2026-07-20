# Elastic Cloud: Create Traffic Filter Ruleset

Creates a new traffic filter ruleset in Elastic Cloud.

```
POST https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/create-traffic-filter-ruleset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/create-traffic-filter-ruleset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/create-traffic-filter-ruleset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | The specification for the traffic filter ruleset. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |

## Native endpoint

Through the native Elastic Cloud API, this operation is `POST /deployments/traffic-filter/rulesets` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-traffic-filter-ruleset.md) for the provider-specific parameters and requirements.

