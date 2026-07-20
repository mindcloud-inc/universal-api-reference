# CueGrowth: Update Campaign



```
PUT https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `campaignId` | string | yes | ID of the campaign. |
| `messageActive` | boolean | no | Whether the invite or first message is active. |
| `followupActive` | boolean | no | Whether the first follow-up is active. |
| `secondFollowupActive` | boolean | no | Whether the second follow-up is active. |
| `thirdFollowupActive` | boolean | no | Whether the third follow-up is active. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "creation_date": "string",
      "filters": "string",
      "followup_active": true,
      "followup_days": 1,
      "followup_message": "string",
      "id": 1,
      "message": "string",
      "message_active": true,
      "name": "Ava Chen",
      "second_followup_active": true,
      "second_followup_days": 1,
      "second_followup_message": "string",
      "third_followup_active": 1,
      "third_followup_days": 1,
      "third_followup_message": "string",
      "type": "string",
      "update_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `creation_date` | string |  |
| `filters` | string |  |
| `followup_active` | boolean |  |
| `followup_days` | number |  |
| `followup_message` | string |  |
| `id` | number |  |
| `message` | string |  |
| `message_active` | boolean |  |
| `name` | string |  |
| `second_followup_active` | boolean |  |
| `second_followup_days` | number |  |
| `second_followup_message` | string |  |
| `third_followup_active` | number |  |
| `third_followup_days` | number |  |
| `third_followup_message` | string |  |
| `type` | string |  |
| `update_date` | string |  |

## Native endpoint

Through the native CueGrowth API, this operation is `PUT /campaigns/{campaign_id}/update` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

