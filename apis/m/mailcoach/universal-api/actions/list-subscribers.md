# Mailcoach: List Subscribers

Retrieves subscribers from a Mailcoach email list.

```
GET https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcoach `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/list-subscribers?connectionId=$CONNECTION_ID&emailListUuid=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "emailListUuid": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailcoach/latest/actions/list-subscribers?${params}`, {
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
| `emailListUuid` | string | yes | The UUID of the email list whose subscribers should be returned. |
| `filterEmail` | string | no | Filter subscribers by exact email address. |
| `filterSearch` | string | no | Fuzzy-search subscribers by email, name, or tags. |
| `filterStatus` | string | no | Filter subscribers by status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "emailListUuid": "ava@example.com",
      "extraAttributes": {},
      "firstName": "Ava",
      "lastName": "Chen",
      "subscribedAt": "2026-05-07T12:00:00.000Z",
      "tags": [
        "string"
      ],
      "unsubscribedAt": "2026-05-07T12:00:00.000Z",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `email` | string |  |
| `emailListUuid` | string |  |
| `extraAttributes` | object |  |
| `firstName` | string |  |
| `lastName` | string |  |
| `subscribedAt` | date |  |
| `tags` | array<string> |  |
| `unsubscribedAt` | date |  |
| `updatedAt` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native Mailcoach API, this operation is `GET /email-lists/:emailListUuid/subscribers` (base URL `https://mindcloud.mailcoach.app/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

