# Channels: List Do Not Call History

Retrieves do-not-call history from Channels.

```
GET https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-do-not-call-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Channels `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-do-not-call-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/channels/latest/actions/list-do-not-call-history?${params}`, {
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
| `dateFrom` | string | no | Optional lower bound for Do Not Call List event date. |
| `dateTo` | string | no | Optional upper bound for Do Not Call List event date. |
| `direction` | string | no | Optional sort direction for Do Not Call List history. |
| `msisdnLike` | string | no | Optional phone-number contains filter. |
| `orderColumn` | string | no | Optional column to order Do Not Call List history by. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "eventDate": "2026-05-07T12:00:00.000Z",
          "msisdn": "string",
          "sameMsisdnEventsCount": 1,
          "status": "string",
          "userId": 1,
          "username": "Ava Chen"
        }
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].eventDate` | date |  |
| `data[].msisdn` | string |  |
| `data[].sameMsisdnEventsCount` | number |  |
| `data[].status` | string |  |
| `data[].userId` | number |  |
| `data[].username` | string |  |
| `total` | number |  |

## Native endpoint

Through the native Channels API, this operation is `GET /api/v1/dnclist` (base URL `https://api.channels.app`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-do-not-call-history.md) for the provider-specific parameters and requirements.

