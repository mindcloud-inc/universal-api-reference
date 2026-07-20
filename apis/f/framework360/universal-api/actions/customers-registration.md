# Framework360: Register Customer



```
POST https://connect.mindcloud.co/v1/universal/framework360/latest/actions/customers-registration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Framework360 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/framework360/latest/actions/customers-registration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "nome": "string",
  "cognome": "string",
  "email": "ava@example.com",
  "password": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/framework360/latest/actions/customers-registration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "nome": "string",
    "cognome": "string",
    "email": "ava@example.com",
    "password": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `nome` | string | yes | Customer first name. |
| `cognome` | string | yes | Customer last name. |
| `email` | string | yes | Customer email address. |
| `password` | string | yes | Customer password. |
| `telefono` | string | no | Customer phone number. |
| `sourceId` | number | no | Customer source ID. |
| `billingData` | object | no | Billing profile data for the customer. |
| `marketingList[]` | array<number> | no | Marketing lists to subscribe the customer to. |
| `marketingActive` | boolean | no | Whether marketing is active for the customer. |
| `tags[]` | array<string> | no | Tags to assign to the customer. |
| `extraFields` | object | no | Custom extra fields for the customer profile. |
| `cart[]` | array<object> | no | Cart associated with the customer. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Framework360 API returns.

## Native endpoint

Through the native Framework360 API, this operation is `POST customers/registration` (base URL `https://mindcloudstage0.framework360.site/m/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/customers-registration.md) for the provider-specific parameters and requirements.

