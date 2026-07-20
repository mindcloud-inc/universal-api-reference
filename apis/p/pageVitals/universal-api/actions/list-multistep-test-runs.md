# PageVitals: List Multistep Test Runs



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-multistep-test-runs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-multistep-test-runs?connectionId=$CONNECTION_ID&websiteId=string&testId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string",
  "testId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-multistep-test-runs?${params}`, {
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
| `testId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bytesTotal": 1,
      "cls": 1,
      "cpuTotal": 1,
      "created": "string",
      "device": "string",
      "duration": 1,
      "id": "string",
      "inp": 1,
      "status": "string",
      "tbt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bytesTotal` | number |  |
| `cls` | number |  |
| `cpuTotal` | number |  |
| `created` | string |  |
| `device` | string |  |
| `duration` | number |  |
| `id` | string |  |
| `inp` | number |  |
| `status` | string |  |
| `tbt` | number |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/multistep/:testId/runs` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-multistep-test-runs.md) for the provider-specific parameters and requirements.

