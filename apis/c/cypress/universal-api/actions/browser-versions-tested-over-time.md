# Cypress: Browser Versions Tested Over Time

Retrieves tested browser versions over time from Cypress Cloud.

```
GET https://connect.mindcloud.co/v1/universal/cypress/latest/actions/browser-versions-tested-over-time
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cypress `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cypress/latest/actions/browser-versions-tested-over-time?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cypress/latest/actions/browser-versions-tested-over-time?${params}`, {
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
      "browser": "string",
      "day": "string",
      "specCount": 1,
      "version": "string",
      "week": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `browser` | string | Browser name returned by Cypress. |
| `day` | string | Day bucket returned by Cypress. |
| `specCount` | number | Number of specs counted for the browser version. |
| `version` | string | Browser version returned by Cypress. |
| `week` | string | Week bucket returned by Cypress. |

## Native endpoint

Through the native Cypress API, this operation is `GET /` (base URL `https://cloud.cypress.io/enterprise-reporting/report`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/browser-versions-tested-over-time.md) for the provider-specific parameters and requirements.

