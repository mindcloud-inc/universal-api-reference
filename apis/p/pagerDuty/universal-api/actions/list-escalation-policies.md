# PagerDuty: List Escalation Policies



```
GET https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-escalation-policies
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagerDuty `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-escalation-policies?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-escalation-policies?${params}`, {
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
| `query` | string | no | Filter escalation policies by a free-text search query. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "escalationRules": [
        "string"
      ],
      "htmlUrl": "https://example.com",
      "id": "string",
      "name": "Ava Chen",
      "numLoops": 1,
      "onCallHandoffNotifications": "string",
      "privilege": "string",
      "self": "string",
      "services": [
        "string"
      ],
      "summary": "string",
      "teams": [
        "string"
      ],
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
| `createdAt` | date | When the policy was created. |
| `description` | string | The escalation policy description. |
| `escalationRules` | array | Escalation rules in the policy. |
| `htmlUrl` | string | The PagerDuty web URL for the escalation policy. |
| `id` | string | The escalation policy ID. |
| `name` | string | The escalation policy name. |
| `numLoops` | number | The number of escalation loops. |
| `onCallHandoffNotifications` | string | How handoff notifications are handled. |
| `privilege` | string | Privilege information for the policy. |
| `self` | string | The API URL for the escalation policy. |
| `services` | array | Services attached to the escalation policy. |
| `summary` | string | PagerDuty's short summary for the escalation policy. |
| `teams` | array | Teams attached to the escalation policy. |
| `type` | string | The PagerDuty object type. |
| `updatedAt` | date | When the policy was last updated. |

## Native endpoint

Through the native PagerDuty API, this operation is `GET /escalation_policies` (base URL `https://api.pagerduty.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-escalation-policies.md) for the provider-specific parameters and requirements.

