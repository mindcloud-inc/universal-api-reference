# Cypress: Accessibility Score Details

Retrieves accessibility score details from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/accessibility-score-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/accessibility-score-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/accessibility-score-details?${params}`, {
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
      "ciBuildId": "string",
      "commitAuthorName": "Ava Chen",
      "commitBranch": "string",
      "createdAt": "string",
      "projectName": "Ava Chen",
      "runNumber": 1,
      "runTags": [
        "string"
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibilityScore` | number | Accessibility score for the run. |
| `ciBuildId` | string | CI build identifier returned by Cypress. |
| `commitAuthorName` | string | Commit author name returned by Cypress. |
| `commitBranch` | string | Commit branch returned by Cypress. |
| `createdAt` | string | Timestamp when the run was created. |
| `projectName` | string | Cypress project name returned by the report. |
| `runNumber` | number | Run number returned by Cypress. |
| `runTags` | array<string> | Run tags returned by Cypress. |
| `status` | string | Run status returned by Cypress. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/accessibility-score-details.md) for the provider-specific parameters and requirements.

