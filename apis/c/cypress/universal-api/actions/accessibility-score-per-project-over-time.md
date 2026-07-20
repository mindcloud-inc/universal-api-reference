# Cypress: Accessibility Score Per Project Over Time

Retrieves accessibility scores per project over time from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/accessibility-score-per-project-over-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/accessibility-score-per-project-over-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/accessibility-score-per-project-over-time?${params}`, {
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
      "accessibilityScore": 1,
      "day": "string",
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
| `accessibilityScore` | number | Accessibility score returned by Cypress for the project. |
| `day` | string | Day bucket returned by Cypress. |
| `projectName` | string | Cypress project name returned by the report. |
| `week` | string | Week bucket returned by Cypress. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accessibility-score-per-project-over-time.md) for the provider-specific parameters and requirements.

