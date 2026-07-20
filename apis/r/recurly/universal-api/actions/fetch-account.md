# Recurly: Fetch Account



```
GET https://connect.mindcloud.co/v1/universal/recurly/latest/actions/fetch-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recurly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/fetch-account?connectionId=$CONNECTION_ID&accountId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/recurly/latest/actions/fetch-account?${params}`, {
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
| `accountId` | string | yes | Recurly account ID or code. |

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

Through the native Recurly API, this operation is `GET /accounts/:account_id` (base URL `https://v3.recurly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-account.md) for the provider-specific parameters and requirements.

