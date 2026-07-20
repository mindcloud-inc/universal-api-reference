# Cypress: Status By Spec

Retrieves spec status rates from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/status-by-spec
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/status-by-spec?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/status-by-spec?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reportId` | string | no | Fixed Cypress report identifier for Status by spec. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "status": "string",
      "testRunCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `status` | string | Spec status label returned by Cypress. |
| `testRunCount` | number | Number of specs in this status bucket. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/status-by-spec.md) for the provider-specific parameters and requirements.

