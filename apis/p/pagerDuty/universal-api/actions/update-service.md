# PagerDuty: Update Service



```
PUT https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/update-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagerDuty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/update-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "service.escalationPolicy.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/update-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "service.escalationPolicy.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The PagerDuty service ID to update. |
| `service.name` | string | no | The updated service name. |
| `service.description` | string | no | The updated service description. |
| `service.escalationPolicy.id` | string | yes | The updated escalation policy ID. |

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

Through the native PagerDuty API, this operation is `PUT /services/:id` (base URL `https://api.pagerduty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service.md) for the provider-specific parameters and requirements.

