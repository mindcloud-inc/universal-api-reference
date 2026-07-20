# Phonely: Duplicate Agent

Creates a duplicate agent in Phonely.

```
POST https://connect.mindcloud.co/v1/universal/phonely/latest/actions/duplicate-agent
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Phonely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/phonely/latest/actions/duplicate-agent" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "uid": "W4LT4yDethRPfyCn9YAEVeIqrDf1",
  "agentId": "DEByI53KCaooZWAGF8jU"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/phonely/latest/actions/duplicate-agent', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "uid": "W4LT4yDethRPfyCn9YAEVeIqrDf1",
    "agentId": "DEByI53KCaooZWAGF8jU"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `uid` | string | yes | Your Phonely user ID. Example: `W4LT4yDethRPfyCn9YAEVeIqrDf1`. |
| `agentId` | string | yes | The ID of the agent to duplicate. Example: `DEByI53KCaooZWAGF8jU`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agentId": "string",
      "name": "Ava Chen",
      "uid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agentId` | string |  |
| `name` | string |  |
| `uid` | string |  |

## Native endpoint

Through the native Phonely API, this operation is `POST /api/duplicate-agent` (base URL `https://app.phonely.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/duplicate-agent.md) for the provider-specific parameters and requirements.

