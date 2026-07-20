# Camio: List Connected Cameras

Retrieves connected cameras from Camio.

```
GET https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-connected-cameras
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Camio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-connected-cameras?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/camio/latest/actions/list-connected-cameras?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cameraId": "string",
      "capabilities": [
        "string"
      ],
      "isOnline": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cameraId` | string | The Camio camera id. |
| `capabilities` | array<string> | Capabilities reported for the camera. |
| `isOnline` | boolean | Whether Camio considers the camera online. |
| `name` | string | The camera name. |

## Native endpoint

Through the native Camio API, this operation is `GET /users/me/cameras/` (base URL `https://camio.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-connected-cameras.md) for the provider-specific parameters and requirements.

