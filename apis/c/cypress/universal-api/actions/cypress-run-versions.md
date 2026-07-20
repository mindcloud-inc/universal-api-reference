# Cypress: Cypress Run Versions

Retrieves Cypress run versions from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-run-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-run-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/cypress-run-versions?${params}`, {
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
      "runCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cypressVersion` | string | Cypress version returned by the report. |
| `runCount` | number | Number of Cypress runs counted for the version. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/cypress-run-versions.md) for the provider-specific parameters and requirements.

