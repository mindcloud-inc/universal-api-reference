# Cypress: Flaky Rate Per Project Over Time

Retrieves flaky rates per project over time from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/flaky-rate-per-project-over-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/flaky-rate-per-project-over-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/flaky-rate-per-project-over-time?${params}`, {
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
      "day": "string",
      "flakyRate": 1,
      "flakyTestCount": 1,
      "passTestCount": 1,
      "projectName": "Ava Chen",
      "week": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `day` | string | Day bucket returned by Cypress. |
| `flakyRate` | number | Flaky rate percentage reported by Cypress. |
| `flakyTestCount` | number | Number of flaky tests counted for the project. |
| `passTestCount` | number | Number of passing tests counted for the project. |
| `projectName` | string | Cypress project name returned by the report. |
| `week` | string | Week bucket returned by Cypress. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/flaky-rate-per-project-over-time.md) for the provider-specific parameters and requirements.

