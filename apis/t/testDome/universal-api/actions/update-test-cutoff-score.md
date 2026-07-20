# TestDome: Update Test Cutoff Score

Updates a test cutoff score in TestDome.

```
PUT https://connect.mindcloud.co/v1/universal/testDome/latest/actions/update-test-cutoff-score
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/update-test-cutoff-score" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cutoffScore": 1,
  "testId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/update-test-cutoff-score', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cutoffScore": 1,
    "testId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cutoffScore` | number | yes |  |
| `testId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expectedPassRate": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expectedPassRate` | number | The expected pass rate (percentage of candidates expected to pass) after updating the cutoff score of a test. |

## Native endpoint

Through the native TestDome API, this operation is `PATCH /tests/:testId/cutoff-score` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-test-cutoff-score.md) for the provider-specific parameters and requirements.

