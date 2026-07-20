# Salesforge: Update Sequence

Updates a sequence in Salesforge.

```
PUT https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/update-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/update-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
  "sequenceID": "seq_q266pc1d33ozbe3et0mes"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/update-sequence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
    "sequenceID": "seq_q266pc1d33ozbe3et0mes"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceID` | string | yes | Workspace ID for the sequence. Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `sequenceID` | string | yes | Sequence ID to update. Example: `seq_q266pc1d33ozbe3et0mes`. |
| `name` | string | no | Updated name for the sequence. Example: `MindCloud Sequence Test Updated`. |
| `productId` | string | no | Updated product ID for the sequence. Example: `prod_jd08oo3u4jlay80n209cr`. |
| `language` | string | no | Updated language for the sequence. Example: `american_english`. |
| `timezone` | string | no | Updated timezone for the sequence. Example: `America/New_York`. |
| `openTrackingEnabled` | boolean | no | Whether open tracking is enabled. Example: `true`. |
| `clickTrackingEnabled` | boolean | no | Whether click tracking is enabled. Example: `true`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforge API returns.

## Native endpoint

Through the native Salesforge API, this operation is `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sequence.md) for the provider-specific parameters and requirements.

