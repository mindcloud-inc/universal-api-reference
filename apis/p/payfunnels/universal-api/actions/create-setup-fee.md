# Payfunnels: Create Setup Fee

Creates a new setup fee in Payfunnels.

```
POST https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/create-setup-fee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Payfunnels `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/create-setup-fee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "amount": 1,
  "currency": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/payfunnels/latest/actions/create-setup-fee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "amount": 1,
    "currency": "string",
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `amount` | number | yes | Amount to charge for the setup fee. |
| `currency` | string | yes | Currency code for the setup fee. |
| `name` | string | yes | Name of the setup fee. |
| `setAsDefault` | boolean | no | Set true to mark this setup fee as the default. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "amount": 1,
      "currency": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `amount` | number |  |
| `currency` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Payfunnels API, this operation is `POST /v1/fees/setup` (base URL `https://api.payfunnels.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-setup-fee.md) for the provider-specific parameters and requirements.

