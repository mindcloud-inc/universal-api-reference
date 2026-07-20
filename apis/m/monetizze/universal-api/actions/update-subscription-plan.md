# Monetizze: Update Subscription Plan

Updates an existing subscription plan in Monetizze.

```
PUT https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/update-subscription-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monetizze `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/update-subscription-plan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscriptionId": 1,
  "newPlanId": 1,
  "billingPolicy": "string",
  "customerEmail": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/monetizze/latest/actions/update-subscription-plan', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscriptionId": 1,
    "newPlanId": 1,
    "billingPolicy": "string",
    "customerEmail": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `subscriptionId` | number | yes | Active subscription code to update. |
| `newPlanId` | number | yes | Target plan code for the upgrade or downgrade. |
| `billingPolicy` | string | yes | Billing policy such as com_credito or valor_inteiro. |
| `customerEmail` | string | yes | Subscriber email address. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assinatura": {},
      "mensagens": [
        "string"
      ],
      "pagamento": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assinatura` | object | Updated subscription summary when the operation succeeds. |
| `mensagens` | array<string> | Provider messages for the subscription update. |
| `pagamento` | object | Payment summary for the upgrade or downgrade charge. |
| `status` | number | Subscription update result code returned by Monetizze. |

## Native endpoint

Through the native Monetizze API, this operation is `POST /assinatura/atualizar` (base URL `https://api.monetizze.com.br/2.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-subscription-plan.md) for the provider-specific parameters and requirements.

