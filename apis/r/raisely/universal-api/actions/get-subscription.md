# Raisely: Get Subscription

Retrieves a subscription from Raisely.

```
GET https://connect.mindcloud.co/v1/universal/raisely/latest/actions/get-subscription
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raisely `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/raisely/latest/actions/get-subscription?connectionId=$CONNECTION_ID&uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uuid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/raisely/latest/actions/get-subscription?${params}`, {
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
| `uuid` | string | yes | The `uuid` of the record |
| `private` | boolean | no | Returns the full record when authenticated |

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

Through the native Raisely API, this operation is `GET /subscriptions/:uuid` (base URL `https://api.raisely.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-subscription.md) for the provider-specific parameters and requirements.

