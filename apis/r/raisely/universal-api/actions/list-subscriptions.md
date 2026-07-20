# Raisely: List Subscriptions

Retrieves subscriptions from Raisely.

```
GET https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raisely/latest/actions/list-subscriptions?${params}`, {
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
| `private` | boolean | no | Returns the full record when authenticated |
| `q` | string | no | Search query to find records matching |
| `mode` | string | no | Filter Subscription based on their mode value |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `status` | string | no | Filter Subscription based on their status value |
| `source` | string | no | Filter subscriptions based on their source value of "OFFLINE" or "ONLINE" |
| `userUuid` | string | no | Filter Subscription based on their userUuid value |
| `campaign` | string | no | Filter by campaign path or uuid |
| `organisation` | string | no | Filter by organisation uuid |
| `profile` | string | no | Filter by profile path or uuid |
| `user` | string | no | Filter by user uuid |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "campaignUuid": "string",
      "count": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "email": "ava@example.com",
      "failed": true,
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "interval": "string",
      "lastName": "Chen",
      "method": "string",
      "mode": "string",
      "nextPayment": "2026-05-07T12:00:00.000Z",
      "profileUuid": "string",
      "source": "string",
      "status": "string",
      "total": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userUuid": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `campaignUuid` | string |  |
| `count` | number |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `email` | string |  |
| `failed` | boolean |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `interval` | string |  |
| `lastName` | string |  |
| `method` | string |  |
| `mode` | string |  |
| `nextPayment` | date |  |
| `profileUuid` | string |  |
| `source` | string |  |
| `status` | string |  |
| `total` | number |  |
| `updatedAt` | date |  |
| `userUuid` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Raisely API, this operation is `GET /subscriptions` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-subscriptions.md) for the provider-specific parameters and requirements.

