# Cypress: Cypress Test Types

Retrieves Cypress test type adoption data from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-test-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-test-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-test-types?${params}`, {
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
      "testingType": "string",
      "totalCt": 1,
      "totalE2e": 1,
      "totalTests": 1,
      "week": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `day` | string | Day bucket returned by Cypress when applicable. |
| `testingType` | string | Cypress testing type such as e2e or component. |
| `totalCt` | number | Total component tests counted in the report row. |
| `totalE2e` | number | Total end-to-end tests counted in the report row. |
| `totalTests` | number | Total tests counted in the report row. |
| `week` | string | Week bucket returned by Cypress when applicable. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cypress-test-types.md) for the provider-specific parameters and requirements.

