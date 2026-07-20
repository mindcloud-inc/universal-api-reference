# MailerLite: List Groups

Retrieves a page of groups from MailerLite.

```
GET https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MailerLite `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailerLite/latest/actions/list-groups?${params}`, {
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
| `limit` | number | no | Number of groups per page. Example: `25`. |
| `page` | number | no | Page number to fetch, starting from 1. Example: `1`. |
| `filter[name]` | string | no | Return groups whose names partially match this value. Example: `VIP`. |
| `sort` | string | no | Sort groups by a supported field, optionally prefixed with - for descending order. Example: `-created_at`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activeCount": 1,
      "bouncedCount": 1,
      "clickRate": {},
      "clicksCount": 1,
      "createdAt": "string",
      "id": "string",
      "junkCount": 1,
      "name": "Ava Chen",
      "openRate": {},
      "opensCount": 1,
      "sentCount": 1,
      "unconfirmedCount": 1,
      "unsubscribedCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activeCount` | number |  |
| `bouncedCount` | number |  |
| `clickRate` | object |  |
| `clicksCount` | number |  |
| `createdAt` | string |  |
| `id` | string |  |
| `junkCount` | number |  |
| `name` | string |  |
| `openRate` | object |  |
| `opensCount` | number |  |
| `sentCount` | number |  |
| `unconfirmedCount` | number |  |
| `unsubscribedCount` | number |  |

## Native endpoint

Through the native MailerLite API, this operation is `GET /groups` (base URL `https://connect.mailerlite.com/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

