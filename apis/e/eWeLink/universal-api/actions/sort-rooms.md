# eWeLink: Sort Rooms

Updates room order in eWeLink.

```
PUT https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/sort-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eWeLink `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/sort-rooms" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eWeLink/latest/actions/sort-rooms', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "error": 1,
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | number |  |
| `msg` | string |  |

## Native endpoint

Through the native eWeLink API, this operation is `POST /v2/family/room/index` (base URL `https://{{credentials.authorizeRequest.region}}-apia.coolkit.cc`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sort-rooms.md) for the provider-specific parameters and requirements.

