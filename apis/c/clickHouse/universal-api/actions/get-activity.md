# ClickHouse: Get Activity



```
GET https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickHouse `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-activity?connectionId=$CONNECTION_ID&organizationId=string&activityId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string",
  "activityId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickHouse/latest/actions/get-activity?${params}`, {
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
| `organizationId` | string | yes | ID of the requested organization. |
| `activityId` | string | yes | ID of the requested activity. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "actorDetails": "string",
      "actorId": "string",
      "actorIpAddress": "string",
      "actorType": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "organizationId": "string",
      "serviceId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `actorDetails` | string | Actor details. |
| `actorId` | string | Actor ID. |
| `actorIpAddress` | string | Actor IP address, when present. |
| `actorType` | string | Actor type. |
| `createdAt` | date | Activity timestamp. |
| `id` | string | Activity ID. |
| `organizationId` | string | Organization ID. |
| `serviceId` | string | Service ID, when the activity is service-scoped. |
| `type` | string | Activity event type. |

## Native endpoint

Through the native ClickHouse API, this operation is `GET /v1/organizations/[:organizationId]/activities/[:activityId]` (base URL `https://api.clickhouse.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-activity.md) for the provider-specific parameters and requirements.

