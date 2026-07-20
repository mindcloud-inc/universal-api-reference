# SeaX: Create General Call Campaign

Creates a general call campaign in SeaX.

```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-general-call-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-general-call-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-general-call-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_time": "string",
      "end_time": "string",
      "id": "string",
      "invalid_destinations": [
        "string"
      ],
      "invalid_destinations_count": 1,
      "name": "Ava Chen",
      "start_time": "string",
      "type": "string",
      "valid_destinations_count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_time` | string |  |
| `end_time` | string |  |
| `id` | string |  |
| `invalid_destinations` | array<string> |  |
| `invalid_destinations_count` | number |  |
| `name` | string |  |
| `start_time` | string |  |
| `type` | string |  |
| `valid_destinations_count` | number |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /general_campaigns/call` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-general-call-campaign.md) for the provider-specific parameters and requirements.

