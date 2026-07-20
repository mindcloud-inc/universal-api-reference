# PayWhirl: List Subscribers

Retrieves subscribers from PayWhirl.

```
GET https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-subscribers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-subscribers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-subscribers?${params}`, {
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
| `keyword` | string | no | Optional keyword filter. |
| `limit` | number | no | Number of subscriber records to return. |
| `order` | string | no | Overall result order. Use asc, desc, or rand. |
| `orderDirection` | string | no | Sort direction. Use asc or desc. |
| `orderKey` | string | no | Subscriber field to sort by. |
| `startingAfter` | number | no | Return subscribers with subscription IDs greater than this value. |
| `startingBefore` | number | no | Return subscribers with subscription IDs lower than this value. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "currentPeriodEnd": 1,
      "currentPeriodStart": 1,
      "customerId": 1,
      "email": "ava@example.com",
      "firstName": "Ava",
      "installmentPlan": 1,
      "installmentsLeft": 1,
      "lastName": "Chen",
      "planId": 1,
      "profile": [
        {
          "answer": "string",
          "label": "string",
          "name": "Ava Chen"
        }
      ],
      "quantity": 1,
      "subscriptionId": 1,
      "updatedAt": "string",
      "userId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `currentPeriodEnd` | number |  |
| `currentPeriodStart` | number |  |
| `customerId` | number |  |
| `email` | string |  |
| `firstName` | string |  |
| `installmentPlan` | number |  |
| `installmentsLeft` | number |  |
| `lastName` | string |  |
| `planId` | number |  |
| `profile[].answer` | string |  |
| `profile[].label` | string |  |
| `profile[].name` | string |  |
| `quantity` | number |  |
| `subscriptionId` | number |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native PayWhirl API, this operation is `GET /subscribers` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-subscribers.md) for the provider-specific parameters and requirements.

