# Cypress: Average Run Duration Over Time

Retrieves average run durations over time from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/average-run-duration-over-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/average-run-duration-over-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/average-run-duration-over-time?${params}`, {
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
      "avgPassRunDuration": 1,
      "day": "string",
      "maxPassRunDuration": 1,
      "mdnPassRunDuration": 1,
      "minPassRunDuration": 1,
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
| `avgPassRunDuration` | number | Average passing run duration in milliseconds. |
| `day` | string | Day bucket returned by Cypress. |
| `maxPassRunDuration` | number | Maximum passing run duration in milliseconds. |
| `mdnPassRunDuration` | number | Median passing run duration in milliseconds. |
| `minPassRunDuration` | number | Minimum passing run duration in milliseconds. |
| `projectName` | string | Cypress project name returned by the report. |
| `runCount` | number | Number of runs counted in the period. |
| `week` | string | Week bucket returned by Cypress. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/average-run-duration-over-time.md) for the provider-specific parameters and requirements.

