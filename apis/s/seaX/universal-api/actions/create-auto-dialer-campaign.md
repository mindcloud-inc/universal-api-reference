# SeaX: Create Auto Dialer Campaign

Creates an auto dialer campaign in SeaX.

```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-auto-dialer-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-auto-dialer-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "captureKeypress": true,
  "captureStt": true,
  "mode": "string",
  "name": "Ava Chen",
  "phoneIds": "string",
  "stage": "string",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-auto-dialer-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "captureKeypress": true,
    "captureStt": true,
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
| `captureKeypress` | boolean | yes | Whether to capture keypad input. |
| `captureStt` | boolean | yes | Whether to capture speech-to-text. |
| `mode` | string | yes | Auto dialer mode. |
| `name` | string | yes | Auto dialer campaign name. |
| `phoneIds` | list<string> | yes | Phone identifiers to call from. |
| `stage` | string | yes | Auto dialer stage. |
| `type` | string | yes | Auto dialer campaign type. |

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
| `type` | object |  |
| `updated_time` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /auto_dialer_campaigns` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-auto-dialer-campaign.md) for the provider-specific parameters and requirements.

