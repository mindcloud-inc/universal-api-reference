# DataForSEO: Get Bulk Traffic Estimation

Retrieves bulk traffic estimates from DataForSEO.

```
GET https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-bulk-traffic-estimation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DataForSEO `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-bulk-traffic-estimation?connectionId=$CONNECTION_ID&targets%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "targets[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dataForSEO/latest/actions/get-bulk-traffic-estimation?${params}`, {
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
| `targets[]` | array<string> | yes | Domains or URLs to estimate traffic for in bulk. |
| `location_name` | string | no | Location context for the DataForSEO Labs analysis. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `language_code` | string | no | Language code for the analysis context. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "metrics": {},
      "target": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `metrics` | object | Estimated keyword and traffic metrics for the target. |
| `target` | string | Target domain evaluated for traffic estimation. |

## Native endpoint

Through the native DataForSEO API, this operation is `POST /v3/dataforseo_labs/bulk_traffic_estimation/live.ai` (base URL `https://api.dataforseo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-bulk-traffic-estimation.md) for the provider-specific parameters and requirements.

