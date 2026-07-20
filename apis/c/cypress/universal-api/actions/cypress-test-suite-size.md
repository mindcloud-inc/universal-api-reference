# Cypress: Cypress Test Suite Size

Retrieves Cypress test suite size data from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-test-suite-size
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-test-suite-size?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-test-suite-size?${params}`, {
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
| `totalCt` | number | Average component tests returned by Cypress for the period. |
| `totalE2e` | number | Average end-to-end tests returned by Cypress for the period. |
| `totalTests` | number | Average total tests returned by Cypress for the period. |
| `week` | string | Week bucket returned by Cypress. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cypress-test-suite-size.md) for the provider-specific parameters and requirements.

