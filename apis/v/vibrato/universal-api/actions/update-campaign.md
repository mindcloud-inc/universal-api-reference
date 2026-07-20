# Vibrato: Update campaign

Updates an existing campaign in Vibrato.

```
PUT https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vibrato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uuid": "string",
  "name": "Ava Chen",
  "taskPropertyToContactField": {},
  "taskTemplateUuid": "string",
  "dailyAvailability[]": [
    {}
  ],
  "timezone": "America/New_York"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uuid": "string",
    "name": "Ava Chen",
    "taskPropertyToContactField": {},
    "taskTemplateUuid": "string",
    "dailyAvailability[]": [{}],
    "timezone": "America/New_York"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uuid` | string | yes | UUID from Vibrato. |
| `name` | string | yes | Campaign name. |
| `taskPropertyToContactField` | object | yes | Mapping from task property slugs to contact fields. |
| `taskTemplateUuid` | string | yes | Task template UUID. |
| `dailyAvailability[]` | array<object> | yes | Daily availability windows. |
| `timezone` | string | yes | Campaign timezone. Default: `America/New_York`. |
| `paused` | boolean | no | Whether the campaign is paused. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_uuids": [
        "string"
      ],
      "completed_campaign_calls": 1,
      "daily_availability": [
        {}
      ],
      "in_progress_campaign_calls": 1,
      "invalid_campaign_calls": 1,
      "name": "Ava Chen",
      "paused": true,
      "queued_campaign_calls": 1,
      "task_property_to_contact_field": {},
      "task_template": {},
      "task_template_uuid": "string",
      "timezone": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_uuids` | array<string> |  |
| `completed_campaign_calls` | number |  |
| `daily_availability` | array<object> |  |
| `in_progress_campaign_calls` | number |  |
| `invalid_campaign_calls` | number |  |
| `name` | string |  |
| `paused` | boolean |  |
| `queued_campaign_calls` | number |  |
| `task_property_to_contact_field` | object |  |
| `task_template` | object |  |
| `task_template_uuid` | string |  |
| `timezone` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Vibrato API, this operation is `PATCH /campaigns/{uuid}/` (base URL `https://api.getvibrato.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

