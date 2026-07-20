# EasyPost: List Pickups

Retrieves a list of pickups from EasyPost.

```
GET https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-pickups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyPost `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-pickups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyPost/latest/actions/list-pickups?${params}`, {
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
      "confirmation": "string",
      "id": "string",
      "maxDatetime": "2026-05-07T12:00:00.000Z",
      "minDatetime": "2026-05-07T12:00:00.000Z",
      "mode": "string",
      "object": "string",
      "pickupRates": [
        {}
      ],
      "reference": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confirmation` | string |  |
| `id` | string |  |
| `maxDatetime` | date |  |
| `minDatetime` | date |  |
| `mode` | string |  |
| `object` | string |  |
| `pickupRates` | array<object> |  |
| `reference` | string |  |
| `status` | string |  |

## Native endpoint

Through the native EasyPost API, this operation is `GET /pickups` (base URL `https://api.easypost.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-pickups.md) for the provider-specific parameters and requirements.

