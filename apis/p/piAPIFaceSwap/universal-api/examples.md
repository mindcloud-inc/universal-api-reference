# PiAPI/FaceSwap Universal API Examples

These examples use the MindCloud API key and PiAPI/FaceSwap connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves account details from PiAPI/FaceSwap.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/get-account-info?${params}`, {
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
        "max_concurrent_task_count": 1,
        "name": "Ava Chen",
        "plan": "string",
        "platform": "string",
        "type": "string",
        "wallet": {}
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIFaceSwap/latest/actions/get-account-info).

## Image Faceswap

Creates an image faceswap task in PiAPI/FaceSwap.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/image-faceswap" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.targetImage": "string",
  "input.swapImage": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIFaceSwap/latest/actions/image-faceswap', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.targetImage": "string",
    "input.swapImage": "string"
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
        "error": {
          "code": 1,
          "detail": {},
          "message": "string",
          "raw_message": "string"
        },
        "input": {},
        "logs": [
          {}
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

See the full [Image Faceswap action reference](actions/image-faceswap.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIFaceSwap/latest/actions/image-faceswap).
