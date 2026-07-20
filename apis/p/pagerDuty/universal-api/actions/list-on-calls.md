# PagerDuty: List On-Calls



```
GET https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-on-calls
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PagerDuty `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-on-calls?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pagerDuty/latest/actions/list-on-calls?${params}`, {
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
| `since` | date | no | Return on-calls starting from this date and time. |
| `until` | date | no | Return on-calls up to this date and time. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "end": "2026-05-07T12:00:00.000Z",
      "escalationLevel": 1,
      "escalationPolicy": {
        "htmlUrl": "https://example.com",
        "id": "string",
        "self": "string",
        "summary": "string",
        "type": "string"
      },
      "schedule": {},
      "start": "2026-05-07T12:00:00.000Z",
      "user": {
        "htmlUrl": "https://example.com",
        "id": "string",
        "self": "string",
        "summary": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `end` | date | When the on-call window ends. |
| `escalationLevel` | number | The escalation level currently on call. |
| `escalationPolicy` | object | The escalation policy currently on call. |
| `escalationPolicy.htmlUrl` | string | The PagerDuty web URL for the escalation policy. |
| `escalationPolicy.id` | string | The escalation policy ID. |
| `escalationPolicy.self` | string | The API URL for the escalation policy. |
| `escalationPolicy.summary` | string | PagerDuty's short summary for the escalation policy. |
| `escalationPolicy.type` | string | The PagerDuty object type for the escalation policy. |
| `schedule` | object | The schedule currently on call. |
| `start` | date | When the on-call window starts. |
| `user` | object | The user currently on call. |
| `user.htmlUrl` | string | The PagerDuty web URL for the on-call user. |
| `user.id` | string | The on-call user ID. |
| `user.self` | string | The API URL for the on-call user. |
| `user.summary` | string | PagerDuty's short summary for the on-call user. |
| `user.type` | string | The PagerDuty object type for the on-call user. |

## Native endpoint

Through the native PagerDuty API, this operation is `GET /oncalls` (base URL `https://api.pagerduty.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-on-calls.md) for the provider-specific parameters and requirements.

