# Instantly: Create Campaign

Creates a new campaign in Instantly.

```
POST https://connect.mindcloud.co/v1/universal/instantly/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "campaignSchedule": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "campaignSchedule": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name of the campaign. |
| `campaignSchedule` | object | yes | Campaign schedule object. |
| `sequences[]` | array<object> | no | Campaign email sequence array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_schedule": {},
      "id": "string",
      "name": "Ava Chen",
      "open_tracking": true,
      "organization": "string",
      "status": 1,
      "timestamp_created": "2026-05-07T12:00:00.000Z",
      "timestamp_updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_schedule` | object |  |
| `id` | string |  |
| `name` | string |  |
| `open_tracking` | boolean |  |
| `organization` | string |  |
| `status` | number |  |
| `timestamp_created` | date |  |
| `timestamp_updated` | date |  |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/campaigns` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

