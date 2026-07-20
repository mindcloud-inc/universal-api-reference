# BoxHero: Update Partner

Updates an existing partner in BoxHero.

```
PUT https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/update-partner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/update-partner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "partnerId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/update-partner', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "partnerId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | no | Address of the partner |
| `email` | string | no | Email address of the partner |
| `memo` | string | no | Notes for the partner |
| `name` | string | no | Name of the partner |
| `partnerId` | number | yes | Unique identifier for the partner |
| `phone` | string | no | Contact number of the partner |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native BoxHero API, this operation is `PUT /v1/partners/:partner_id` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-partner.md) for the provider-specific parameters and requirements.

