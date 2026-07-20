# TikTok Conversions: Create Offline Event Set

Creates a new Offline Event set in TikTok Conversions.

```
POST https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/create-offline-event-set
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Conversions `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/create-offline-event-set" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "advertiser_id": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tikTokConversions/latest/actions/create-offline-event-set', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "advertiser_id": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `advertiser_id` | string | yes |  |
| `name` | string | yes |  |
| `auto_tracking` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "data": {
        "event_set_id": "string"
      },
      "message": "string",
      "request_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `data` | object |  |
| `data.event_set_id` | string |  |
| `message` | string |  |
| `request_id` | string |  |

## Native endpoint

Through the native TikTok Conversions API, this operation is `POST /open_api/v1.3/offline/create/` (base URL `https://business-api.tiktok.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-offline-event-set.md) for the provider-specific parameters and requirements.

