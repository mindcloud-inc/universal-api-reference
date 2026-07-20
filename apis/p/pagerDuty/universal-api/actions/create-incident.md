# PagerDuty: Create Incident



```
POST https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/create-incident
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagerDuty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/create-incident" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "incident.title": "string",
  "incident.service.id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/create-incident', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "incident.title": "string",
    "incident.service.id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `incident.title` | string | yes | A short description of the incident. |
| `incident.service.id` | string | yes | The PagerDuty service ID for the incident. |
| `incident.urgency` | string | no | The incident urgency. |
| `incident.incidentKey` | string | no | A de-duplication key for the incident. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "escalationPolicy": {
        "id": "string",
        "summary": "string",
        "type": "string"
      },
      "htmlUrl": "https://example.com",
      "id": "string",
      "incidentKey": "string",
      "incidentNumber": 1,
      "priority": {
        "id": "string",
        "summary": "string",
        "type": "string"
      },
      "self": "string",
      "service": {
        "htmlUrl": "https://example.com",
        "id": "string",
        "self": "string",
        "summary": "string",
        "type": "string"
      },
      "status": "string",
      "summary": "string",
      "title": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "urgency": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | When the incident was first triggered. |
| `escalationPolicy` | object | The escalation policy for the incident. |
| `escalationPolicy.id` | string | The escalation policy ID. |
| `escalationPolicy.summary` | string | PagerDuty's short summary for the escalation policy. |
| `escalationPolicy.type` | string | The PagerDuty object type for the escalation policy. |
| `htmlUrl` | string | The PagerDuty web URL for the incident. |
| `id` | string | The PagerDuty incident ID. |
| `incidentKey` | string | The incident de-duplication key. |
| `incidentNumber` | number | The incident number unique to the account. |
| `priority` | object | The incident priority. |
| `priority.id` | string | The priority ID. |
| `priority.summary` | string | PagerDuty's short summary for the priority. |
| `priority.type` | string | The PagerDuty object type for the priority. |
| `self` | string | The API URL for the incident. |
| `service` | object | The service attached to the incident. |
| `service.htmlUrl` | string | The PagerDuty web URL for the service. |
| `service.id` | string | The service ID. |
| `service.self` | string | The API URL for the service. |
| `service.summary` | string | PagerDuty's short summary for the service. |
| `service.type` | string | The PagerDuty object type for the service. |
| `status` | string | The current incident status. |
| `summary` | string | PagerDuty's short summary for the incident. |
| `title` | string | The incident title. |
| `type` | string | The PagerDuty object type. |
| `updatedAt` | date | When the incident was last modified. |
| `urgency` | string | The incident urgency level. |

## Native endpoint

Through the native PagerDuty API, this operation is `POST /incidents` (base URL `https://api.pagerduty.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-incident.md) for the provider-specific parameters and requirements.

