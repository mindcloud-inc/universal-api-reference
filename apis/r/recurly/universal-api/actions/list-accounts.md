# Recurly: List Accounts



```
GET https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-accounts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recurly `connectionId` ([setup](../authentication.md)).

This action also supports [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-accounts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurly/latest/actions/list-accounts?${params}`, {
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
| `beginTime` | string | no | Only return accounts created or updated on or after this timestamp. |
| `email` | string | no | Filter accounts by email address. |
| `endTime` | string | no | Only return accounts created or updated before this timestamp. |
| `ids` | string | no | Filter by one or more account IDs. |
| `subscriber` | boolean | no | Only return accounts that currently have or had subscriptions. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "company": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "hasActiveSubscription": true,
      "hasLiveSubscription": true,
      "hasPastDueInvoice": true,
      "id": "string",
      "lastName": "Chen",
      "object": "string",
      "preferredLocale": "string",
      "preferredTimeZone": "string",
      "state": "string",
      "taxExempt": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string |  |
| `company` | string |  |
| `createdAt` | date |  |
| `deletedAt` | date |  |
| `email` | string |  |
| `firstName` | string |  |
| `hasActiveSubscription` | boolean |  |
| `hasLiveSubscription` | boolean |  |
| `hasPastDueInvoice` | boolean |  |
| `id` | string |  |
| `lastName` | string |  |
| `object` | string |  |
| `preferredLocale` | string |  |
| `preferredTimeZone` | string |  |
| `state` | string |  |
| `taxExempt` | boolean |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Recurly API, this operation is `GET /accounts` (base URL `https://v3.recurly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-accounts.md) for the provider-specific parameters and requirements.

