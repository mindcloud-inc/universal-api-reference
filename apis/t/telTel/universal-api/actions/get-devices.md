# TelTel: Get Devices

Retrieves devices from your TelTel account.

```
GET https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TelTel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-devices?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/telTel/latest/actions/get-devices?${params}`, {
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
      "isOnline": true,
      "name": "Ava Chen",
      "realname": "Ava Chen",
      "stateId": 1,
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `isOnline` | boolean |  |
| `name` | string |  |
| `realname` | string |  |
| `stateId` | number |  |
| `userId` | number |  |

## Native endpoint

Through the native TelTel API, this operation is `GET /devices` (base URL `https://api.teltel.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-devices.md) for the provider-specific parameters and requirements.

