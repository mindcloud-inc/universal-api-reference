# Cypress: UI Coverage Per Project

Retrieves UI coverage per project from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/u-i-coverage-per-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/u-i-coverage-per-project?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/u-i-coverage-per-project?${params}`, {
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
      "uiCoveragePct": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `projectName` | string | Cypress project name returned by the report. |
| `uiCoveragePct` | number | UI coverage percentage reported by Cypress for the project. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/u-i-coverage-per-project.md) for the provider-specific parameters and requirements.

