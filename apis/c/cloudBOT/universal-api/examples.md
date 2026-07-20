# Cloud BOT Universal API Examples

These examples use the MindCloud API key and Cloud BOT connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contracts

Retrieves contracts from Cloud BOT.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-contracts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/list-contracts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "code": 1,
      "department": "string",
      "location": "string",
      "name": "Ava Chen",
      "organization": "string",
      "owner": "string",
      "phone": "string",
      "plan": "string",
      "postcode": "string",
      "publicId": "string",
      "publicPath": "string",
      "timezone": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Contracts action reference](actions/list-contracts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudBOT/latest/actions/list-contracts).

## Create Bot Subscription

Creates a bot subscription in Cloud BOT.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/create-bot-subscription" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicId": "string",
  "botId": "string",
  "event": "string",
  "callbackType": "webhook",
  "callbackEndpoint": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cloudBOT/latest/actions/create-bot-subscription', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicId": "string",
    "botId": "string",
    "event": "string",
    "callbackType": "webhook",
    "callbackEndpoint": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "subscribeId": 1,
      "unsubscribeEndpoint": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Bot Subscription action reference](actions/create-bot-subscription.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudBOT/latest/actions/create-bot-subscription).
