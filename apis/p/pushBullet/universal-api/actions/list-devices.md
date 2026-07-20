# Pushbullet: List Devices

Retrieves devices from your Pushbullet account.

```
GET https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/list-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pushbullet `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/list-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pushBullet/latest/actions/list-devices?${params}`, {
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
      "active": true,
      "created": 1,
      "iden": "string",
      "manufacturer": "string",
      "model": "string",
      "modified": 1,
      "nickname": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `created` | number |  |
| `iden` | string |  |
| `manufacturer` | string |  |
| `model` | string |  |
| `modified` | number |  |
| `nickname` | string |  |

## Native endpoint

Through the native Pushbullet API, this operation is `GET /devices` (base URL `https://api.pushbullet.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-devices.md) for the provider-specific parameters and requirements.

