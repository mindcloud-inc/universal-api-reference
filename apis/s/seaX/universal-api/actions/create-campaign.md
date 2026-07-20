# SeaX: Create Campaign

Creates a campaign in the current SeaX workspace.

```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "messageServiceId": "string",
  "mode": "string",
  "name": "Ava Chen",
  "phoneIds": "string",
  "stage": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "messageServiceId": "string",
    "mode": "string",
    "name": "Ava Chen",
    "phoneIds": "string",
    "stage": "string",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `messageServiceId` | string | yes | Messaging service identifier. |
| `mode` | string | yes | Campaign mode. |
| `name` | string | yes | Campaign name. |
| `phoneIds` | list<string> | yes | Phone identifiers to send from. |
| `stage` | string | yes | Campaign stage. |
| `type` | string | yes | Campaign type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_time": "string",
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": {},
      "type": {},
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_time` | string |  |
| `id` | string |  |
| `message` | string |  |
| `name` | string |  |
| `status` | object |  |
| `type` | object |  |
| `updated_time` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /campaigns` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign.md) for the provider-specific parameters and requirements.

