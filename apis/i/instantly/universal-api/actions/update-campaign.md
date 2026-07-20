# Instantly: Update Campaign

Updates an existing campaign in Instantly.

```
PUT https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instantly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instantly/latest/actions/update-campaign', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Campaign ID. |
| `name` | string | yes | Updated campaign name. |

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

Through the native Instantly API, this operation is `PATCH /api/v2/campaigns/:id` (base URL `https://api.instantly.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-campaign.md) for the provider-specific parameters and requirements.

