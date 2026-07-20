# Vibrato: Retrieve campaign

Retrieves a specific campaign from Vibrato.

```
GET https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vibrato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-campaign?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/retrieve-campaign?${params}`, {
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
| `uuid` | string | yes | UUID from Vibrato. |

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

Through the native Vibrato API, this operation is `GET /campaigns/{uuid}/` (base URL `https://api.getvibrato.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-campaign.md) for the provider-specific parameters and requirements.

