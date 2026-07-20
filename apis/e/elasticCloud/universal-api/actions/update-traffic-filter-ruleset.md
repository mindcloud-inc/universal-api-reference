# Elastic Cloud: Update Traffic Filter Ruleset

Updates an existing traffic filter ruleset in Elastic Cloud.

```
PUT https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/update-traffic-filter-ruleset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/update-traffic-filter-ruleset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "body": {},
  "rulesetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/update-traffic-filter-ruleset', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "body": {},
    "rulesetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `body` | object | yes | The specification for the traffic filter ruleset. |
| `rulesetId` | string | yes | Identifier for the ruleset. |

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

Through the native Elastic Cloud API, this operation is `PUT /deployments/traffic-filter/rulesets/:ruleset_id` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-traffic-filter-ruleset.md) for the provider-specific parameters and requirements.

