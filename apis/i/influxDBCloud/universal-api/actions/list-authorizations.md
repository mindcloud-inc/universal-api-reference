# InfluxDB Cloud: List Authorizations

Retrieves authorizations from InfluxDB Cloud.

```
GET https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-authorizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InfluxDB Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-authorizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influxDBCloud/latest/actions/list-authorizations?${params}`, {
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
| `limit` | number | no | Maximum number of authorizations to return. Default: `1`. |
| `orgId` | string | no | Organization ID to scope the authorization list. Default: `{{credentials.orgId}}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "links": {},
      "org": "string",
      "orgID": "string",
      "permissions": [
        {}
      ],
      "status": "string",
      "token": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "user": "string",
      "userID": "string"
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
| `links` | object |  |
| `org` | string |  |
| `orgID` | string |  |
| `permissions` | array<object> |  |
| `status` | string |  |
| `token` | string |  |
| `updatedAt` | date |  |
| `user` | string |  |
| `userID` | string |  |

## Native endpoint

Through the native InfluxDB Cloud API, this operation is `GET /authorizations` (base URL `https://us-east-1-1.aws.cloud2.influxdata.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-authorizations.md) for the provider-specific parameters and requirements.

