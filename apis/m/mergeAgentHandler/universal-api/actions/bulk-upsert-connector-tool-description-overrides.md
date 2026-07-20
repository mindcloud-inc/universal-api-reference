# Merge Agent Handler: Bulk Upsert Connector Tool Description Overrides

Upserts or deletes connector tool description overrides in Merge Agent Handler.

```
PUT https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/bulk-upsert-connector-tool-description-overrides
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merge Agent Handler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/bulk-upsert-connector-tool-description-overrides" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/bulk-upsert-connector-tool-description-overrides', {
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



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merge Agent Handler API returns.

## Native endpoint

Through the native Merge Agent Handler API, this operation is `PATCH /connectors/tool-description-overrides/` (base URL `https://ah-api.merge.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/bulk-upsert-connector-tool-description-overrides.md) for the provider-specific parameters and requirements.

