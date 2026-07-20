# SuperSend: Update Sender

Updates an existing sender in SuperSend.

```
PUT https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-sender
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-sender" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/superSend/latest/actions/update-sender', {
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
| `sendAs` | string | no |  |
| `replyTo` | string | no |  |
| `signature` | string | no |  |
| `forwardTo` | string | no |  |
| `forwardRules[]` | array<object> | no | Per-destination forwarding rules. Each rule maps email destinations to optional label filters. |
| `forwardRules[].emails` | string | no | Comma-separated email addresses for this rule Accepts multiple values in one string, delimited by `,`. |
| `forwardRules[].labelIds[]` | array<string> | no |  |
| `disabled` | boolean | no |  |
| `warm` | boolean | no |  |
| `maxPerDay` | number | no | Range: 1 to 15000. |
| `globalMaxPerDay` | number | no | Range: 1 to 1000. |
| `maxWarmPerDay` | number | no | Range: 1 to 1000. |
| `warmEmailRamp` | number | no | Range: 1 to 365. |
| `campaignRampEnabled` | boolean | no |  |
| `campaignRampDurationDays` | number | no | Days to reach target (required when ramp enabled) Range: 1 to 365. |
| `campaignRampStartVolume` | number | no | Limit on first send day (required when ramp enabled) Range: 1 to inf. |
| `senderProfileId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_ramp_duration_days": 1,
      "campaign_ramp_enabled": true,
      "campaign_ramp_first_send_date": "2026-05-07T12:00:00.000Z",
      "campaign_ramp_start_volume": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "disabled": true,
      "domain": "string",
      "email": "ava@example.com",
      "forward_rules": [
        {
          "emails": "ava@example.com",
          "label_ids": [
            [
              "string"
            ]
          ]
        }
      ],
      "forward_to": "string",
      "global_max_per_day": 1,
      "health_score": 1,
      "id": "string",
      "max_per_day": 1,
      "max_warm_per_day": 1,
      "provider": "string",
      "reply_to": "string",
      "send_as": "string",
      "sender_profile": {
        "id": "string",
        "name": "Ava Chen",
        "timezone": "string"
      },
      "signature": "string",
      "status": "string",
      "team_id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "warm": true,
      "warming_stage": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_ramp_duration_days` | number |  |
| `campaign_ramp_enabled` | boolean |  |
| `campaign_ramp_first_send_date` | date |  |
| `campaign_ramp_start_volume` | number |  |
| `created_at` | date |  |
| `disabled` | boolean |  |
| `domain` | string |  |
| `email` | string |  |
| `forward_rules[].emails` | string |  |
| `forward_rules[].label_ids[]` | array<string> |  |
| `forward_to` | string |  |
| `global_max_per_day` | number |  |
| `health_score` | number |  |
| `id` | string |  |
| `max_per_day` | number |  |
| `max_warm_per_day` | number |  |
| `provider` | string |  |
| `reply_to` | string |  |
| `send_as` | string |  |
| `sender_profile.id` | string |  |
| `sender_profile.name` | string |  |
| `sender_profile.timezone` | string |  |
| `signature` | string |  |
| `status` | string |  |
| `team_id` | string |  |
| `updated_at` | date |  |
| `warm` | boolean |  |
| `warming_stage` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `PATCH /senders/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-sender.md) for the provider-specific parameters and requirements.

