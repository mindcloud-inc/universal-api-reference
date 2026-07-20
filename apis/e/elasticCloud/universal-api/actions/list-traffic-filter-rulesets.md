# Elastic Cloud: List Traffic Filter Rulesets

Retrieves traffic filter rulesets from Elastic Cloud.

```
GET https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-traffic-filter-rulesets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Elastic Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-traffic-filter-rulesets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/elasticCloud/latest/actions/list-traffic-filter-rulesets?${params}`, {
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
| `includeAssociations` | boolean | no | Include resources associated with each ruleset. |
| `organizationId` | string | no | Limit rulesets to the specified organization ID. Only takes effect for admins. |
| `region` | string | no | Limit rulesets to the specified region. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Elastic Cloud API returns.

## Native endpoint

Through the native Elastic Cloud API, this operation is `GET /deployments/traffic-filter/rulesets` (base URL `https://api.elastic-cloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-traffic-filter-rulesets.md) for the provider-specific parameters and requirements.

