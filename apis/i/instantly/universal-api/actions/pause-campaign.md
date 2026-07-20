# Instantly: Pause Campaign

Pauses a campaign in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/pause-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/pause-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/pause-campaign', {
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
| `id` | string | yes | Campaign ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_schedule": {},
      "id": "string",
      "name": "Ava Chen",
      "status": 1,
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
| `status` | number |  |
| `timestamp_updated` | date |  |

## Native endpoint

Through the native Instantly API, this operation is `POST /api/v2/campaigns/:id/pause` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/pause-campaign.md) for the provider-specific parameters and requirements.

