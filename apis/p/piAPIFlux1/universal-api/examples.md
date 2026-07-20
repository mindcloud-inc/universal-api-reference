# PiAPI/Flux.1 Universal API Examples

These examples use the MindCloud API key and PiAPI/Flux.1 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves your account information from PiAPI/Flux.1.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/get-account-info?${params}`, {
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
        "equivalent_in_usd": 1,
        "id": 1,
        "is_enable": true,
        "max_concurrent_task_count": 1,
        "name": "Ava Chen",
        "plan": "string",
        "wallet": {
          "mj_remain": 1,
          "point_remain": 1
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIFlux1/latest/actions/get-account-info).

## Create Flux ControlNet LoRA Task

Creates a Flux ControlNet LoRA task in PiAPI/Flux.1.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/create-flux-control-net-lo-ra-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "string",
  "input.controlNetSettings[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIFlux1/latest/actions/create-flux-control-net-lo-ra-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "string",
    "input.controlNetSettings[]": ["string"]
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
        "config": {
          "service_mode": "string",
          "webhook_config": {
            "endpoint": "string",
            "secret": "string"
          }
        },
        "error": {
          "code": 1,
          "message": "string",
          "raw_message": "string"
        },
        "input": {},
        "logs": [
          {}
        ],
        "meta": {
          "created_at": "string",
          "ended_at": "string",
          "is_using_private_pool": true,
          "started_at": "string",
          "usage": {
            "consume": 1,
            "frozen": 1,
            "type": "string"
          }
        },
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

See the full [Create Flux ControlNet LoRA Task action reference](actions/create-flux-control-net-lo-ra-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIFlux1/latest/actions/create-flux-control-net-lo-ra-task).
