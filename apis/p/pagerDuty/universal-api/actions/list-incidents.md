# PagerDuty: List Incidents



```
GET https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-incidents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagerDuty `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-incidents?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-incidents?${params}`, {
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
| `dateRange` | string | no | Set to all to ignore the default since and until range. |
| `incidentKey` | string | no | Filter incidents by incident de-duplication key. |
| `serviceIds[]` | array<string> | no | Return only incidents associated with these service IDs. |
| `teamIds[]` | array<string> | no | Return only incidents related to these team IDs. |
| `userIds[]` | array<string> | no | Return only incidents currently assigned to these user IDs. |
| `urgencies[]` | array<string> | no | Return only incidents with these urgency values. |
| `timeZone` | string | no | Time zone used when rendering the results. |
| `statuses[]` | array<string> | no | Return only incidents with these statuses. |
| `include[]` | array<string> | no | Include additional incident details in the response. |
| `since` | date | no | Start of the incident search time range. |
| `until` | date | no | End of the incident search time range. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignments": [
        "string"
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "escalationPolicy": {
        "htmlUrl": "https://example.com",
        "id": "string",
        "self": "string",
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
      "teams": [
        "string"
      ],
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
| `assignments` | array | Current assignments on the incident. |
| `createdAt` | date | When the incident was first triggered. |
| `escalationPolicy` | object | The escalation policy for the incident. |
| `escalationPolicy.htmlUrl` | string | The PagerDuty web URL for the escalation policy. |
| `escalationPolicy.id` | string | The escalation policy ID. |
| `escalationPolicy.self` | string | The API URL for the escalation policy. |
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
| `teams` | array | Teams involved in the incident. |
| `title` | string | The incident title. |
| `type` | string | The PagerDuty object type. |
| `updatedAt` | date | When the incident was last modified. |
| `urgency` | string | The incident urgency level. |

## Native endpoint

Through the native PagerDuty API, this operation is `GET /incidents` (base URL `https://api.pagerduty.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-incidents.md) for the provider-specific parameters and requirements.

