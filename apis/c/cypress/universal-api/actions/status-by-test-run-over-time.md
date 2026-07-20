# Cypress: Status By Test Run Over Time

Retrieves individual test status rates over time from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/status-by-test-run-over-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/status-by-test-run-over-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/status-by-test-run-over-time?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "projectName": "Ava Chen",
      "status": "string",
      "testRunCount": 1,
      "week": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectName` | string | Cypress project name returned by the report. |
| `status` | string | Test status label returned by Cypress. |
| `testRunCount` | number | Number of test results counted in the status bucket. |
| `week` | string | Week bucket returned by Cypress. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/status-by-test-run-over-time.md) for the provider-specific parameters and requirements.

