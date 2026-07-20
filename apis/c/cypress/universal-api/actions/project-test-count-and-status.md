# Cypress: Project Test Count And Status

Retrieves project test counts and statuses from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/project-test-count-and-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/project-test-count-and-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/project-test-count-and-status?${params}`, {
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
| `day` | string | Day bucket returned by Cypress. |
| `projectName` | string | Cypress project name returned by the report. |
| `status` | string | Status bucket returned by Cypress. |
| `testRunCount` | number | Number of test runs counted in the bucket. |
| `week` | string | Week bucket returned by Cypress. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/project-test-count-and-status.md) for the provider-specific parameters and requirements.

