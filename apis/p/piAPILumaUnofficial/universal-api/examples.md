# PiAPI/Luma (unofficial) Universal API Examples

These examples use the MindCloud API key and PiAPI/Luma (unofficial) connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get PiAPI Account Info

Retrieves connected account details from PiAPI.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/get-piapi-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/get-piapi-account-info?${params}`, {
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
      "code": 1,
      "data": {
        "id": 1,
        "name": "Ava Chen",
        "plan": "string",
        "platform": "string",
        "type": "string",
        "wallet": {
          "luma_remain": 1
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get PiAPI Account Info action reference](actions/get-piapi-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPILumaUnofficial/latest/actions/get-piapi-account-info).

## Create Luma Task

Creates a new Luma task in PiAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/create-luma-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPILumaUnofficial/latest/actions/create-luma-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "string"
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
      "data": {
        "config": {},
        "detail": {},
        "error": {},
        "input": {},
        "logs": [
          "string"
        ],
        "meta": {},
        "model": "string",
        "output": {},
        "status": "string",
        "task_id": "string",
        "task_type": "string"
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Luma Task action reference](actions/create-luma-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPILumaUnofficial/latest/actions/create-luma-task).
