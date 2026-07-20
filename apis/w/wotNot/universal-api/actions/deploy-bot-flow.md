# WotNot: Deploy Bot Flow

Deploys a bot flow in WotNot.

```
PUT https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/deploy-bot-flow
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WotNot `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/deploy-bot-flow" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "botId": 1,
  "flowDiagram": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wotNot/latest/actions/deploy-bot-flow', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "botId": 1,
    "flowDiagram": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `botId` | number | yes | WotNot bot ID |
| `flowDiagram` | string | yes | Bot flow JSON to deploy |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "is_deployed": true,
      "last_deployed_at": "string",
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `is_deployed` | boolean |  |
| `last_deployed_at` | string |  |
| `ok` | boolean |  |

## Native endpoint

Through the native WotNot API, this operation is `POST /v1/bots/:bot_id/deploy` (base URL `https://api.wotnot.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deploy-bot-flow.md) for the provider-specific parameters and requirements.

