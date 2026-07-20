# Ringg AI: Terminate Calls by Call IDs

Terminates active Ringg AI calls by call IDs.

```
PUT https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/terminate-calls-by-call-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ringg AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/terminate-calls-by-call-ids" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ringgAI/latest/actions/terminate-calls-by-call-ids', {
  method: 'PUT',
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `agentId` | string | no | ID of the agent whose calls should be terminated |
| `callIds[]` | array<string> | no | Array of call IDs to terminate |
| `campaignId` | string | no | ID of the campaign whose calls should be terminated |
| `mobileNumbers[]` | array<string> | no | Array of mobile numbers to terminate calls for (max 100) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string |  |

## Native endpoint

Through the native Ringg AI API, this operation is `PATCH /campaign/terminate` (base URL `https://prod-api.ringg.ai/ca/api/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/terminate-calls-by-call-ids.md) for the provider-specific parameters and requirements.

