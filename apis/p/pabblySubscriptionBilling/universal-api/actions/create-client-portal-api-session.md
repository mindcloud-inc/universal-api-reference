# Pabbly Subscription Billing: Create Client Portal API Session



```
POST https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-client-portal-api-session
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pabbly Subscription Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-client-portal-api-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pabblySubscriptionBilling/latest/actions/create-client-portal-api-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | no |  |
| `redirectUrl` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accessUrl": "https://example.com",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customerId": "string",
      "expiresAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "status": "string",
      "token": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accessUrl` | string |  |
| `createdAt` | date |  |
| `customerId` | string |  |
| `expiresAt` | date |  |
| `id` | string |  |
| `status` | string |  |
| `token` | string |  |
| `updatedAt` | date |  |
| `userId` | string |  |

## Native endpoint

Through the native Pabbly Subscription Billing API, this operation is `POST /v1/portal_sessions` (base URL `https://payments.pabbly.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-client-portal-api-session.md) for the provider-specific parameters and requirements.

