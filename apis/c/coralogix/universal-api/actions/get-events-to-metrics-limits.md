# Coralogix: Get Events To Metrics Limits



```
GET https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/get-events-to-metrics-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coralogix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/get-events-to-metrics-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/coralogix/latest/actions/get-events-to-metrics-limits?${params}`, {
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
      "companyId": "string",
      "labelsLimit": 1,
      "metricsLimit": {},
      "permutationsLimit": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `companyId` | string | companyId returned by Coralogix. |
| `labelsLimit` | number | labelsLimit returned by Coralogix. |
| `metricsLimit` | object | metricsLimit returned by Coralogix. |
| `permutationsLimit` | object | permutationsLimit returned by Coralogix. |

## Native endpoint

Through the native Coralogix API, this operation is `GET /events2metrics/events2metrics/v2/limits` (base URL `https://api.eu2.coralogix.com/mgmt/openapi/latest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-events-to-metrics-limits.md) for the provider-specific parameters and requirements.

