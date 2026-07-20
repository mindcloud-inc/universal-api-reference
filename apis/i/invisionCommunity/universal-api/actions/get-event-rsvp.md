# Invision Community: Get Event RSVP



```
GET https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-event-rsvp
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invision Community `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-event-rsvp?connectionId=$CONNECTION_ID&id=1&member_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "member_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invisionCommunity/latest/actions/get-event-rsvp?${params}`, {
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
| `id` | number | yes | Event identifier. |
| `member_id` | number | yes | Member identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "memberId": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `memberId` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Invision Community API, this operation is `GET /calendar/events/:id/rsvps/:member_id` (base URL `{{credentials.communityBaseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-event-rsvp.md) for the provider-specific parameters and requirements.

