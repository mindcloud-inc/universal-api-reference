# Salesforge: Update Sequence Steps

Updates sequence steps in Salesforge.

```
PUT https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/update-sequence-steps
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/update-sequence-steps" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
  "sequenceID": "seq_q266pc1d33ozbe3et0mes",
  "steps[]": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/update-sequence-steps', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
    "sequenceID": "seq_q266pc1d33ozbe3et0mes",
    "steps[]": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceID` | string | yes | Workspace ID for the sequence. Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `sequenceID` | string | yes | Sequence ID to update steps for. Example: `seq_q266pc1d33ozbe3et0mes`. |
| `steps[]` | array<object> | yes | Array of sequence steps to update. Example: `[object Object]`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforge API returns.

## Native endpoint

Through the native Salesforge API, this operation is `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID/steps` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sequence-steps.md) for the provider-specific parameters and requirements.

