# Level: List Devices

Retrieves a list of devices from Level.

```
GET https://connect.mindcloud.co/v1/universal/level/latest/actions/list-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Level `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/level/latest/actions/list-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/level/latest/actions/list-devices?${params}`, {
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
      "data": [
        {
          "groupId": "string",
          "hostname": "Ava Chen",
          "id": "string",
          "online": true,
          "platform": "string"
        }
      ],
      "hasMore": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].groupId` | string |  |
| `data[].hostname` | string |  |
| `data[].id` | string |  |
| `data[].online` | boolean |  |
| `data[].platform` | string |  |
| `hasMore` | boolean |  |

## Native endpoint

Through the native Level API, this operation is `GET /devices` (base URL `https://api.level.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-devices.md) for the provider-specific parameters and requirements.

