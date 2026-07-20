# InfluxDB Cloud: Get Organization Limits

Retrieves organization limits from InfluxDB Cloud.

```
GET https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/get-organization-limits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InfluxDB Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/get-organization-limits?connectionId=$CONNECTION_ID&orgId=%7B%7Bcredentials.orgId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "{{credentials.orgId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/get-organization-limits?${params}`, {
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
| `orgId` | string | yes | InfluxDB organization ID. Default: `{{credentials.orgId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "limits": {},
      "links": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `limits` | object |  |
| `links` | object |  |

## Native endpoint

Through the native InfluxDB Cloud API, this operation is `GET /orgs/:orgID/limits` (base URL `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-limits.md) for the provider-specific parameters and requirements.

