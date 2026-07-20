# MailerLite: List Group Subscribers

Retrieves subscribers from a specific group in MailerLite.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-group-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-group-subscribers?connectionId=$CONNECTION_ID&group_id=180900000000000001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "group_id": "180900000000000001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-group-subscribers?${params}`, {
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
| `group_id` | string | yes | Existing MailerLite group identifier. Example: `180900000000000001`. |
| `filter[status]` | string | no | Return subscribers with this status. One of: `0`, `1`, `2`, `3`, `4`. |
| `limit` | number | no | Number of subscribers to return. Example: `50`. |
| `cursor` | string | no | Pagination cursor from a previous response. Example: `eyJpZCI6IjE4MDg2MzE1NyJ9`. |
| `include` | string | no | Additional resources to include in the response. One of: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clickRate": 1,
      "clicksCount": 1,
      "createdAt": "string",
      "email": "ava@example.com",
      "id": "string",
      "ipAddress": "string",
      "openRate": 1,
      "opensCount": 1,
      "optedInAt": "string",
      "optinIp": "string",
      "sent": 1,
      "source": "string",
      "status": "string",
      "subscribedAt": "string",
      "unsubscribedAt": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clickRate` | number |  |
| `clicksCount` | number |  |
| `createdAt` | string |  |
| `email` | string |  |
| `id` | string |  |
| `ipAddress` | string |  |
| `openRate` | number |  |
| `opensCount` | number |  |
| `optedInAt` | string |  |
| `optinIp` | string |  |
| `sent` | number |  |
| `source` | string |  |
| `status` | string |  |
| `subscribedAt` | string |  |
| `unsubscribedAt` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /groups/:group_id/subscribers` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-group-subscribers.md) for the provider-specific parameters and requirements.

