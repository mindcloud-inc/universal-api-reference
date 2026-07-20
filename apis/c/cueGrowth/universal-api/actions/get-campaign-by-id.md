# CueGrowth: Get Campaign By Id



```
GET https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/get-campaign-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CueGrowth `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/get-campaign-by-id?connectionId=$CONNECTION_ID&campaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "campaignId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cueGrowth/latest/actions/get-campaign-by-id?${params}`, {
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
| `campaignId` | string | yes | ID of the campaign. |

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

Through the native CueGrowth API, this operation is `GET /campaigns/{campaign_id}` (base URL `https://api.cuegrowth.ai/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-campaign-by-id.md) for the provider-specific parameters and requirements.

