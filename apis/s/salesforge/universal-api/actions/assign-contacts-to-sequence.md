# Salesforge: Assign Contacts To Sequence

Assigns contacts to a sequence in Salesforge.

```
PUT https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/assign-contacts-to-sequence
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Salesforge `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/assign-contacts-to-sequence" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
  "sequenceID": "seq_q266pc1d33ozbe3et0mes",
  "contactIds[]": "cnt_123456"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/assign-contacts-to-sequence', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceID": "wks_989gtkhm1ir6z8hdv3gjn",
    "sequenceID": "seq_q266pc1d33ozbe3et0mes",
    "contactIds[]": "cnt_123456"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceID` | string | yes | Workspace ID for the sequence. Example: `wks_989gtkhm1ir6z8hdv3gjn`. |
| `sequenceID` | string | yes | Sequence ID to assign contacts to. Example: `seq_q266pc1d33ozbe3et0mes`. |
| `contactIds[]` | array<string> | yes | Contact IDs to assign to the sequence. Example: `cnt_123456`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Salesforge API returns.

## Native endpoint

Through the native Salesforge API, this operation is `PUT /public/v2/workspaces/:workspaceID/sequences/:sequenceID/contacts` (base URL `https://api.salesforge.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/assign-contacts-to-sequence.md) for the provider-specific parameters and requirements.

