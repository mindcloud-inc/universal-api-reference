# TestDome: Cancel Candidate Invite

Cancels a candidate invite in TestDome.

```
PUT https://connect.mindcloud.co/v1/universal/testDome/latest/actions/cancel-candidate-invite
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/cancel-candidate-invite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "candidateId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/cancel-candidate-invite', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "candidateId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `candidateId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TestDome API returns.

## Native endpoint

Through the native TestDome API, this operation is `POST /candidates/:candidateId/cancel-invite` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cancel-candidate-invite.md) for the provider-specific parameters and requirements.

