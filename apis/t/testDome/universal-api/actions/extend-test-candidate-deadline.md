# TestDome: Extend Test Candidate Deadline

Extends test candidate deadlines in TestDome.

```
PUT https://connect.mindcloud.co/v1/universal/testDome/latest/actions/extend-test-candidate-deadline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/extend-test-candidate-deadline" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "testId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/extend-test-candidate-deadline', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "testId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `candidateIds` | list<number> | no |  |
| `newDeadline` | string | no |  |
| `testId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "failedCandidateIds": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `failedCandidateIds` | array<number> | The list of candidates, which deadline's couldn't be extended, represented by their IDs. |

## Native endpoint

Through the native TestDome API, this operation is `PUT /tests/:testId/candidates/deadline` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/extend-test-candidate-deadline.md) for the provider-specific parameters and requirements.

