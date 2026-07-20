# TestDome: Get Test Settings

Retrieves test settings from TestDome.

```
GET https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-test-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TestDome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-test-settings?connectionId=$CONNECTION_ID&testId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "testId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/testDome/latest/actions/get-test-settings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `testId` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_links": {},
      "databaseOptions": [
        "string"
      ],
      "description": "string",
      "integrationDeadlineInDays": 1,
      "integrationProctoring": true,
      "isAiForbidden": true,
      "name": "Ava Chen",
      "notifyTo": [
        "string"
      ],
      "showFinalScoreToCandidate": true,
      "timingPolicy": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_links` | object | Dictionary |
| `databaseOptions` | array<string> | If the test contains multi-sql questions, this setting defines databases that can be used by the candidate. |
| `description` | string | The description of the test. |
| `integrationDeadlineInDays` | number | Gets or sets the deadline in days for candidates invited through integration. |
| `integrationProctoring` | boolean | Gets or sets whether invites would have Proctoring enabled for candidates invited through integration. |
| `isAiForbidden` | boolean | Gets or sets whether AI tools are forbidden for candidates taking this test. |
| `name` | string | The name of the test. |
| `notifyTo` | array<string> | Defines the email addresses of those that will be notified when a candidate finishes this test. |
| `showFinalScoreToCandidate` | boolean | Defines if candidates are able to see their score when they finish the test. |
| `timingPolicy` | string | Defines the timing policy of the test, to decide how strict is the time limit enforcement. strict: Candidates will have the exact amount of time defined by the question. normal: Candidates will have the amount of time with an extra 50% buffer. relaxed: Candidates will have the amount of time with an extra 200% buffer. |

## Native endpoint

Through the native TestDome API, this operation is `GET /tests/:testId/settings` (base URL `https://api.staging.testdome.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-test-settings.md) for the provider-specific parameters and requirements.

