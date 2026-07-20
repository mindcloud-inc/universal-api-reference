# TestDome: Update Test Settings

Updates test settings in TestDome.

```
PUT https://connect.mindcloud.co/v1/universal/testDome/latest/actions/update-test-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/update-test-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "showFinalScoreToCandidate": true,
  "testId": 1,
  "timingPolicy": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/testDome/latest/actions/update-test-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "showFinalScoreToCandidate": true,
    "testId": 1,
    "timingPolicy": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `databaseOptions` | list<string> | no |  |
| `description` | string | no |  |
| `integrationDeadlineInDays` | number | no |  |
| `integrationProctoring` | boolean | no |  |
| `isAiForbidden` | boolean | no |  |
| `name` | string | yes |  |
| `notifyTo` | list<string> | no |  |
| `showFinalScoreToCandidate` | boolean | yes |  |
| `testId` | number | yes |  |
| `timingPolicy` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TestDome API returns.

## Native endpoint

Through the native TestDome API, this operation is `PATCH /tests/:testId/settings` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-test-settings.md) for the provider-specific parameters and requirements.

