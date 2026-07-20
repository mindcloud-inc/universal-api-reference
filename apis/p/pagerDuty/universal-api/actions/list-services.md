# PagerDuty: List Services



```
GET https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-services
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagerDuty `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-services?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-services?${params}`, {
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
| `query` | string | no | Filter services by a free-text search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "escalationPolicy": {
        "htmlUrl": "https://example.com",
        "id": "string",
        "self": "string",
        "summary": "string",
        "type": "string"
      },
      "htmlUrl": "https://example.com",
      "id": "string",
      "lastIncidentTimestamp": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "self": "string",
      "status": "string",
      "summary": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the service was created. |
| `description` | string | The service description. |
| `escalationPolicy` | object | The escalation policy attached to the service. |
| `escalationPolicy.htmlUrl` | string | The PagerDuty web URL for the escalation policy. |
| `escalationPolicy.id` | string | The escalation policy ID. |
| `escalationPolicy.self` | string | The API URL for the escalation policy. |
| `escalationPolicy.summary` | string | PagerDuty's short summary for the escalation policy. |
| `escalationPolicy.type` | string | The PagerDuty object type for the escalation policy. |
| `htmlUrl` | string | The PagerDuty web URL for the service. |
| `id` | string | The PagerDuty service ID. |
| `lastIncidentTimestamp` | date | When the most recent incident was created for the service. |
| `name` | string | The service name. |
| `self` | string | The API URL for the service. |
| `status` | string | The current PagerDuty status for the service. |
| `summary` | string | PagerDuty's short summary for the service. |
| `type` | string | The PagerDuty object type. |

## Native endpoint

Through the native PagerDuty API, this operation is `GET /services` (base URL `https://api.pagerduty.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-services.md) for the provider-specific parameters and requirements.

