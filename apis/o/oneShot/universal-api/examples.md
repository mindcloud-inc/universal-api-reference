# 1Shot Universal API Examples

These examples use the MindCloud API key and 1Shot connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Chains

Retrieves supported blockchain networks from 1Shot API.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-chains?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/list-chains?${params}`, {
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
      "averageBlockMiningTime": 1,
      "chainId": 1,
      "name": "Ava Chen",
      "nativeCurrency": {
        "decimals": 1,
        "name": "Ava Chen",
        "symbol": "string"
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Chains action reference](actions/list-chains.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneShot/latest/actions/list-chains).

## Create Contract Event

Creates a new contract event in 1Shot API.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-contract-event" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "businessId": "string",
  "chainId": 1,
  "contractAddress": "string",
  "name": "Ava Chen",
  "description": "string",
  "eventName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneShot/latest/actions/create-contract-event', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "businessId": "string",
    "chainId": 1,
    "contractAddress": "string",
    "name": "Ava Chen",
    "description": "string",
    "eventName": "Ava Chen"
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
      "businessId": "string",
      "chainId": 1,
      "contractAddress": "string",
      "created": 1,
      "description": "string",
      "eventName": "Ava Chen",
      "id": "string",
      "name": "Ava Chen",
      "topicHash": "string",
      "topics": [
        {
          "indexed": true,
          "name": "Ava Chen"
        }
      ],
      "updated": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Contract Event action reference](actions/create-contract-event.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneShot/latest/actions/create-contract-event).
