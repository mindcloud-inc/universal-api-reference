# SuperSend: Update Campaign

Updates an existing campaign in SuperSend.

```
PUT https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Resource ID (UUID) |
| `name` | string | no |  |
| `trackDomain` | string | no |  |
| `track` | boolean | no |  |
| `nodes[]` | array | no |  |
| `edges[]` | array | no |  |
| `status` | number | no | Allowed values: 1, 2. |
| `isDraft` | boolean | no |  |
| `timezone` | string | no |  |
| `days` | object | no |  |
| `hours[]` | array<object> | no |  |
| `hours[].start` | string | no |  |
| `hours[].end` | string | no |  |
| `start` | date | no |  |
| `end` | date | no |  |
| `bcc[]` | array<string> | no |  |
| `bccRepliesOnly` | boolean | no |  |
| `unsubscribe` | boolean | no |  |
| `unsubscribeMessage` | string | no |  |
| `blacklistIfUnsubscribe` | boolean | no |  |
| `blacklistIfBounced` | boolean | no |  |
| `blacklistDomainOnReply` | boolean | no |  |
| `listUnsubscribeHeader` | boolean | no |  |
| `failureConfiguration` | object | no |  |
| `failureConfiguration.strategy` | string | no | Allowed values: skip, retry, pause_contact, pause_campaign. |
| `failureConfiguration.retryAfterDays` | number | no |  |
| `failureConfiguration.notification` | boolean | no |  |
| `sendToRiskLevels[]` | array<string> | no |  |
| `maxPerDay` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "bcc_replies_only": true,
      "bcc": [
        [
          "string"
        ]
      ],
      "blacklistDomainOnReply": true,
      "blacklistIfBounced": true,
      "blacklistIfUnsubscribe": true,
      "bounce_checkpoint_at": "2026-05-07T12:00:00.000Z",
      "contact_count": 1,
      "contact_metrics": {
        "finished": 1,
        "in_progress": 1,
        "not_started": 1,
        "paused": 1,
        "total": 1
      },
      "created_at": "2026-05-07T12:00:00.000Z",
      "days": {},
      "disabled": true,
      "end": "2026-05-07T12:00:00.000Z",
      "failureConfiguration": {
        "notification": true,
        "retryAfterDays": 1,
        "strategy": "string"
      },
      "hours": [
        {
          "end": "string",
          "start": "string"
        }
      ],
      "id": "string",
      "latest_lifecycle_event": {
        "actor": {
          "email": "ava@example.com",
          "id": "string",
          "name": "Ava Chen"
        },
        "event_type": "string",
        "metadata": {},
        "occurred_at": "2026-05-07T12:00:00.000Z",
        "reason_code": "string"
      },
      "list_unsubscribe_header": true,
      "max_per_day": 1,
      "name": "Ava Chen",
      "send_to_risk_levels": [
        [
          "string"
        ]
      ],
      "start": "2026-05-07T12:00:00.000Z",
      "status": "string",
      "team_id": "string",
      "timezone": "string",
      "track": true,
      "track_domain": "string",
      "track_domain_setup_complete": true,
      "track_domain_status": "string",
      "unsubscribe": true,
      "unsubscribe_message": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bcc_replies_only` | boolean |  |
| `bcc[]` | array<string> |  |
| `blacklistDomainOnReply` | boolean |  |
| `blacklistIfBounced` | boolean |  |
| `blacklistIfUnsubscribe` | boolean |  |
| `bounce_checkpoint_at` | date |  |
| `contact_count` | number |  |
| `contact_metrics.finished` | number |  |
| `contact_metrics.in_progress` | number |  |
| `contact_metrics.not_started` | number |  |
| `contact_metrics.paused` | number |  |
| `contact_metrics.total` | number |  |
| `created_at` | date |  |
| `days` | object |  |
| `disabled` | boolean |  |
| `end` | date |  |
| `failureConfiguration.notification` | boolean |  |
| `failureConfiguration.retryAfterDays` | number |  |
| `failureConfiguration.strategy` | string |  |
| `hours[].end` | string |  |
| `hours[].start` | string |  |
| `id` | string |  |
| `latest_lifecycle_event.actor.email` | string |  |
| `latest_lifecycle_event.actor.id` | string |  |
| `latest_lifecycle_event.actor.name` | string |  |
| `latest_lifecycle_event.event_type` | string |  |
| `latest_lifecycle_event.metadata` | object |  |
| `latest_lifecycle_event.occurred_at` | date |  |
| `latest_lifecycle_event.reason_code` | string |  |
| `list_unsubscribe_header` | boolean |  |
| `max_per_day` | number |  |
| `name` | string |  |
| `send_to_risk_levels[]` | array<string> |  |
| `start` | date |  |
| `status` | string |  |
| `team_id` | string |  |
| `timezone` | string |  |
| `track` | boolean |  |
| `track_domain` | string |  |
| `track_domain_setup_complete` | boolean |  |
| `track_domain_status` | string |  |
| `unsubscribe` | boolean |  |
| `unsubscribe_message` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native SuperSend API, this operation is `PATCH /campaigns/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

