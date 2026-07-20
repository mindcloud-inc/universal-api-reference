# Cypress: Cypress Run Versions Per Project Over Time

Retrieves project-level Cypress run versions over time from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-run-versions-per-project-over-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-run-versions-per-project-over-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-run-versions-per-project-over-time?${params}`, {
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
      "cypressVersion": "string",
      "projectName": "Ava Chen",
      "runCount": 1,
      "week": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cypressVersion` | string | Cypress version returned by the report. |
| `projectName` | string | Cypress project name returned by the report. |
| `runCount` | number | Number of Cypress runs counted for the project. |
| `week` | string | Week bucket returned by Cypress. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cypress-run-versions-per-project-over-time.md) for the provider-specific parameters and requirements.

