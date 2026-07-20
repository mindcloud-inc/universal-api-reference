# PayWhirl: List Customer Subscriptions

Retrieves a customer's subscriptions from PayWhirl.

```
GET https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-customer-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PayWhirl `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-customer-subscriptions?connectionId=$CONNECTION_ID&customerId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "customerId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/payWhirl/latest/actions/list-customer-subscriptions?${params}`, {
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
| `customerId` | number | yes | The PayWhirl customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cancelAtPeriodEnd": 1,
      "createdAt": "string",
      "currentPeriodEnd": 1,
      "currentPeriodStart": 1,
      "customerId": 1,
      "deletedAt": "string",
      "id": 1,
      "installmentPlan": 1,
      "installmentsLeft": 1,
      "plan": {
        "billingAmount": 1,
        "id": 1,
        "name": "Ava Chen"
      },
      "planId": 1,
      "quantity": 1,
      "trialEnd": 1,
      "trialStart": 1,
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
| `cancelAtPeriodEnd` | number |  |
| `createdAt` | string |  |
| `currentPeriodEnd` | number |  |
| `currentPeriodStart` | number |  |
| `customerId` | number |  |
| `deletedAt` | string |  |
| `id` | number |  |
| `installmentPlan` | number |  |
| `installmentsLeft` | number |  |
| `plan.billingAmount` | number |  |
| `plan.id` | number |  |
| `plan.name` | string |  |
| `planId` | number |  |
| `quantity` | number |  |
| `trialEnd` | number |  |
| `trialStart` | number |  |
| `updatedAt` | string |  |
| `userId` | number |  |

## Native endpoint

Through the native PayWhirl API, this operation is `GET /subscriptions/{id}` (base URL `https://api.paywhirl.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-customer-subscriptions.md) for the provider-specific parameters and requirements.

