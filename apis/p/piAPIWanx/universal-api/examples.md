# PiAPI/Wanx Universal API Examples

These examples use the MindCloud API key and PiAPI/Wanx connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves account info from PiAPI/Wanx.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/piAPIWanx/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/piAPIWanx/latest/actions/get-account-info?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIWanx/latest/actions/get-account-info).

## Create Image to Video with Camera Control

Creates a camera-controlled video task in PiAPI/Wanx.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/piAPIWanx/latest/actions/create-image-to-video-control-camera" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input.image": "https://i.ibb.co/wbw9GLY/girl.webp",
  "input.control_camera_settings[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/piAPIWanx/latest/actions/create-image-to-video-control-camera', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input.image": "https://i.ibb.co/wbw9GLY/girl.webp",
    "input.control_camera_settings[]": [{}]
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

See the full [Create Image to Video with Camera Control action reference](actions/create-image-to-video-control-camera.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/piAPIWanx/latest/actions/create-image-to-video-control-camera).
