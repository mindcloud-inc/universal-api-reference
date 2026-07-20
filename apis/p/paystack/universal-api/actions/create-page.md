# Paystack: Create Page



```
POST https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paystack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/paystack/latest/actions/create-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `description` | string | no |  |
| `amount` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "amount": 1,
      "createdAt": "string",
      "currency": "string",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "published": true,
      "slug": "string",
      "type": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `amount` | number |  |
| `createdAt` | string |  |
| `currency` | string |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `published` | boolean |  |
| `slug` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Paystack API, this operation is `POST /page` (base URL `https://api.paystack.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page.md) for the provider-specific parameters and requirements.

