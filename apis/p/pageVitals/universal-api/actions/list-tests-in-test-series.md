# PageVitals: List Tests in Test Series



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-tests-in-test-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-tests-in-test-series?connectionId=$CONNECTION_ID&websiteId=string&seriesId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "seriesId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-tests-in-test-series?${params}`, {
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
| `websiteId` | string | yes |  |
| `seriesId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessibilityScore": 1,
      "bestPracticesScore": 1,
      "budgetsAtRisk": 1,
      "budgetsExceeded": 1,
      "created": "string",
      "device": "string",
      "id": "string",
      "opportunityCount": 1,
      "page": {},
      "performanceScore": 1,
      "seoScore": 1,
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessibilityScore` | number |  |
| `bestPracticesScore` | number |  |
| `budgetsAtRisk` | number |  |
| `budgetsExceeded` | number |  |
| `created` | string |  |
| `device` | string |  |
| `id` | string |  |
| `opportunityCount` | number |  |
| `page` | object |  |
| `performanceScore` | number |  |
| `seoScore` | number |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/testseries/:seriesId` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-tests-in-test-series.md) for the provider-specific parameters and requirements.

