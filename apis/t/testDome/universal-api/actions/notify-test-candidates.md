# TestDome: Notify Test Candidates

Notifies test candidates in TestDome.

```
PUT https://connect.mindcloud.co/v1/universal/testDome/latest/actions/notify-test-candidates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/notify-test-candidates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "candidateIds": 1,
  "replyTo": "string",
  "testId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/notify-test-candidates', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "candidateIds": 1,
    "replyTo": "string",
    "testId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `candidateIds` | list<number> | yes |  |
| `failEmail` | string | no |  |
| `passEmail` | string | no |  |
| `replyTo` | string | yes |  |
| `testId` | number | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TestDome API returns.

## Native endpoint

Through the native TestDome API, this operation is `POST /tests/:testId/candidates/notify` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/notify-test-candidates.md) for the provider-specific parameters and requirements.

