# PiAPI/NanoBanana Universal API Examples

These examples use the MindCloud API key and PiAPI/NanoBanana connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPINanoBanana/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPINanoBanana/latest/actions/get-account-info?${params}`, {
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
        "name": "Ava Chen",
        "plan": "string",
        "platform": "string",
        "type": "string",
        "wallet": {
          "gpts_remain": 1,
          "llm_remain": 1,
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

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPINanoBanana/latest/actions/get-account-info).

## Create Gemini 2.5 Flash Image Task



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPINanoBanana/latest/actions/create-gemini25-flash-image-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.prompt": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPINanoBanana/latest/actions/create-gemini25-flash-image-task', {
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
  "data": [],
  "meta": {}
}
```

See the full [Create Gemini 2.5 Flash Image Task action reference](actions/create-gemini25-flash-image-task.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPINanoBanana/latest/actions/create-gemini25-flash-image-task).
