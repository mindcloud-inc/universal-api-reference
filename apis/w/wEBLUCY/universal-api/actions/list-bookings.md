# WEBLUCY: List Bookings

Retrieves bookings from WEBLUCY.

```
GET https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/list-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WEBLUCY `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/list-bookings?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wEBLUCY/latest/actions/list-bookings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `eventId` | string | no | Filter bookings by event ID. |
| `from` | string | no | List only bookings created after this Unix timestamp, inclusive. |
| `to` | string | no | List only bookings created before this Unix timestamp, inclusive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {}
      ],
      "limit": 1,
      "skip": 1,
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `items` | array<object> |  |
| `limit` | number |  |
| `skip` | number |  |
| `totalCount` | number |  |

## Native endpoint

Through the native WEBLUCY API, this operation is `GET /bookings` (base URL `https://apps.weblucy.com/api/site`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-bookings.md) for the provider-specific parameters and requirements.

