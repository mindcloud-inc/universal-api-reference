# Timeular: V2 List all known Devices

Retrieves devices from the Timeular v2 API.

```
GET https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-list-all-known-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Timeular `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-list-all-known-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeular/latest/actions/v2-list-all-known-devices?${params}`, {
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
      "devices": [
        {
          "active": true,
          "disabled": true,
          "name": "Ava Chen",
          "serial": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `devices[].active` | boolean |  |
| `devices[].disabled` | boolean |  |
| `devices[].name` | string |  |
| `devices[].serial` | string |  |

## Native endpoint

Through the native Timeular API, this operation is `GET /api/v2/devices` (base URL `https://api.early.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/v2-list-all-known-devices.md) for the provider-specific parameters and requirements.

