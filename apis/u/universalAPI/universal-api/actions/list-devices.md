# Universal API: List Devices

Retrieves a list of devices from Universal API.

```
GET https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/list-devices
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Universal API `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/list-devices?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/universalAPI/latest/actions/list-devices?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "serialNumber": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `serialNumber` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Universal API API, this operation is `GET /api/mdm/devices` (base URL `https://api.prod.universalapi.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-devices.md) for the provider-specific parameters and requirements.

