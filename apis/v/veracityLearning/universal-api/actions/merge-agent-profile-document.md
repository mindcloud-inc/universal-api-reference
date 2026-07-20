# Veracity Learning: Merge Agent Profile Document

Updates an agent profile document in Veracity Learning by merging content.

```
PUT https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/merge-agent-profile-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veracity Learning `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/merge-agent-profile-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agent": {},
  "profileId": "string",
  "document": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veracityLearning/latest/actions/merge-agent-profile-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agent": {},
    "profileId": "string",
    "document": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agent` | object | yes | xAPI Agent JSON object identifying the learner or actor. |
| `profileId` | string | yes | Exact agent profile document identifier. |
| `document` | object | yes | JSON document patch to merge into this agent profile. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Veracity Learning API returns.

## Native endpoint

Through the native Veracity Learning API, this operation is `POST /agents/profile` (base URL `https://sample-lrs-rafehwe.lrs.io/xapi`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/merge-agent-profile-document.md) for the provider-specific parameters and requirements.

