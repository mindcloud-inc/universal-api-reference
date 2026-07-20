# PiAPI/Skyreels Universal API Examples

These examples use the MindCloud API key and PiAPI/Skyreels connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves information about your PiAPI account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/get-account-info?${params}`, {
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
        "account_group": "string",
        "id": 1,
        "is_enable": true,
        "is_verified": true,
        "max_concurrent_task_count": 1,
        "name": "Ava Chen",
        "plan": "string",
        "platform": "string",
        "type": "string",
        "wallet": {
          "id": 1,
          "point_frozen": 1,
          "point_remain": 1,
          "point_used": 1
        }
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPISkyreels/latest/actions/get-account-info).

## Create Skyreels Task

Creates a new Skyreels task in PiAPI.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/create-skyreels-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "FPS-24, gentle camera move over a portrait photo",
  "input.image": "https://example.com/source-image.png"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPISkyreels/latest/actions/create-skyreels-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.prompt": "FPS-24, gentle camera move over a portrait photo",
    "input.image": "https://example.com/source-image.png"
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
        "input": {
          "aspect_ratio": "string",
          "guidance_scale": 1,
          "image": "string",
          "negative_prompt": "string",
          "prompt": "string"
        },
        "meta": {
          "created_at": "2026-05-07T12:00:00.000Z",
          "ended_at": "2026-05-07T12:00:00.000Z",
          "is_using_private_pool": true,
          "started_at": "2026-05-07T12:00:00.000Z",
          "usage": {
            "consume": 1,
            "frozen": 1,
            "type": "string"
          }
        },
        "model": "string",
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

See the full [Create Skyreels Task action reference](actions/create-skyreels-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPISkyreels/latest/actions/create-skyreels-task).
