# HelpCrunch: Unsubscribe Team Member

Unsubscribes a team member in HelpCrunch.

```
PUT https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/unsubscribe-team-member
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HelpCrunch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/unsubscribe-team-member" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpCrunch/latest/actions/unsubscribe-team-member', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native HelpCrunch API returns.

## Native endpoint

Through the native HelpCrunch API, this operation is `GET /agents/:agentId/unsubscribe` (base URL `https://api.helpcrunch.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-team-member.md) for the provider-specific parameters and requirements.

