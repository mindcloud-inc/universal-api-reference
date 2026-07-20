# InfluxDB Cloud: List Buckets

Retrieves buckets from InfluxDB Cloud.

```
GET https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-buckets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InfluxDB Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-buckets?connectionId=$CONNECTION_ID&orgId=%7B%7Bcredentials.orgId%7D%7D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "orgId": "{{credentials.orgId}}"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-buckets?${params}`, {
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
| `limit` | number | no | Maximum number of buckets to return. Default: `1`. |
| `orgId` | string | yes | InfluxDB organization ID to list buckets for. Default: `{{credentials.orgId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "labels": [
        {}
      ],
      "links": {},
      "name": "Ava Chen",
      "orgID": "string",
      "retentionRules": [
        {}
      ],
      "schemaType": "string",
      "storageType": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `labels` | array<object> |  |
| `links` | object |  |
| `name` | string |  |
| `orgID` | string |  |
| `retentionRules` | array<object> |  |
| `schemaType` | string |  |
| `storageType` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native InfluxDB Cloud API, this operation is `GET /buckets` (base URL `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-buckets.md) for the provider-specific parameters and requirements.

