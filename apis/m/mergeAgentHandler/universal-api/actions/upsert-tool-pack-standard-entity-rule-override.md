# Merge Agent Handler: Upsert Tool Pack Standard Entity Rule Override

Creates or updates a tool pack standard entity rule override in Merge Agent Handler.

```
PUT https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/upsert-tool-pack-standard-entity-rule-override
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merge Agent Handler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/upsert-tool-pack-standard-entity-rule-override" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/upsert-tool-pack-standard-entity-rule-override', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityType` | string | no | Entity type for the standard entity rule. |
| `toolPackId` | string | no | ID of the tool pack. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merge Agent Handler API returns.

## Native endpoint

Through the native Merge Agent Handler API, this operation is `PUT /tool-packs/:tool_pack_id/standard-entity-rules/:entity_type/` (base URL `https://ah-api.merge.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-tool-pack-standard-entity-rule-override.md) for the provider-specific parameters and requirements.

