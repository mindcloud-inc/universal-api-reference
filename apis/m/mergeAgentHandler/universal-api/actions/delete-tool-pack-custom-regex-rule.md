# Merge Agent Handler: Delete Tool Pack Custom Regex Rule

Deletes a tool pack custom regex rule from Merge Agent Handler.

```
DELETE https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/delete-tool-pack-custom-regex-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Merge Agent Handler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/delete-tool-pack-custom-regex-rule?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mergeAgentHandler/latest/actions/delete-tool-pack-custom-regex-rule?${params}`, {
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
| `ruleId` | string | no | ID of the custom regex rule. |
| `toolPackId` | string | no | ID of the tool pack. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Merge Agent Handler API returns.

## Native endpoint

Through the native Merge Agent Handler API, this operation is `DELETE /tool-packs/:tool_pack_id/custom-regex-rules/:rule_id/` (base URL `https://ah-api.merge.dev/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-tool-pack-custom-regex-rule.md) for the provider-specific parameters and requirements.

