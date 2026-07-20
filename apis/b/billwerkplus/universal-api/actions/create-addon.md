# Billwerkplus: Create Add-On

Creates an add-on in Billwerkplus.

```
POST https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-addon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billwerkplus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-addon" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "handle": "string",
  "name": "Ava Chen",
  "amount": 1,
  "type": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/billwerkplus/latest/actions/create-addon', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "handle": "string",
    "name": "Ava Chen",
    "amount": 1,
    "type": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `handle` | string | yes | Per account unique handle for the add-on. |
| `name` | string | yes | Name of add-on. Used as order line text. |
| `amount` | number | yes | Add-on amount. |
| `type` | list | yes | Add-on type: on_off or quantity. One of: `0`, `1`. |
| `allPlans` | boolean | no | Whether all plans are eligible for this add-on. Default: `true`. |
| `amountInclVat` | boolean | no | Whether the amount already includes VAT. Default: `true`. |
| `description` | string | no | Optional description of add-on. |
| `currency` | string | no | Optional ISO 4217 currency code for the add-on. |
| `vat` | number | no | Optional VAT rate for the add-on. |
| `eligiblePlans[]` | array<string> | no | Plan handles eligible for this add-on when all plans is false. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taxPolicy` | string | no | Optional tax policy handle for the add-on. |
| `entitlements[]` | array<string> | no | Entitlement handles for the add-on. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allPlans": true,
      "amount": 1,
      "amountInclVat": true,
      "created": "string",
      "currency": "string",
      "description": "string",
      "handle": "string",
      "name": "Ava Chen",
      "state": "string",
      "type": "string",
      "vat": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allPlans` | boolean |  |
| `amount` | number |  |
| `amountInclVat` | boolean |  |
| `created` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `handle` | string |  |
| `name` | string |  |
| `state` | string |  |
| `type` | string |  |
| `vat` | number |  |

## Native endpoint

Through the native Billwerkplus API, this operation is `POST /add_on` (base URL `https://api.frisbii.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-addon.md) for the provider-specific parameters and requirements.

