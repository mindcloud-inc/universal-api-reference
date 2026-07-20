# Recurly: Update Account



```
PUT https://connect.mindcloud.co/v1/universal/recurly/latest/actions/update-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Recurly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/recurly/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/recurly/latest/actions/update-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Recurly account ID or code. |
| `billTo` | string | no | Billing responsibility setting for hierarchical accounts. |
| `company` | string | no | Updated company name. |
| `email` | string | no | Updated account email address. |
| `firstName` | string | no | Updated billing first name. |
| `lastName` | string | no | Updated billing last name. |
| `preferredLocale` | string | no | Updated preferred locale. |
| `preferredTimeZone` | string | no | Updated preferred time zone. |
| `taxExempt` | boolean | no | Whether the account is tax exempt. |

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

Through the native Recurly API, this operation is `PUT /accounts/:account_id` (base URL `https://v3.recurly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-account.md) for the provider-specific parameters and requirements.

