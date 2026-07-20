# Vibrato: List campaigns

Retrieves a list of campaigns from Vibrato.

```
GET https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/list-campaigns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vibrato `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vibrato/latest/actions/list-campaigns?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Vibrato API, this operation is `GET /campaigns/` (base URL `https://api.getvibrato.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-campaigns.md) for the provider-specific parameters and requirements.

