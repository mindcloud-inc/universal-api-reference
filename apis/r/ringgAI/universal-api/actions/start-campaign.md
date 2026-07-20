# Ringg AI: Start Campaign

Starts a campaign in Ringg AI.

```
POST https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/start-campaign
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/start-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "agentId": "string",
  "listId": "string",
  "fromNumbers[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/start-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "agentId": "string",
    "listId": "string",
    "fromNumbers[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | yes | (Required) ID of the agent that will handle the calls. |
| `listId` | string | yes | (Required) ID of the uploaded campaign contact list. |
| `fromNumbers[]` | array<string> | yes | (Required) Array of phone numbers to use for outbound calls. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hasOngoingCalls": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `hasOngoingCalls` | boolean | Whether the workspace has other ongoing calls |
| `status` | string | Success message indicating campaign registration |

## Native endpoint

Through the native Ringg AI API, this operation is `POST /campaign/start` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-campaign.md) for the provider-specific parameters and requirements.

