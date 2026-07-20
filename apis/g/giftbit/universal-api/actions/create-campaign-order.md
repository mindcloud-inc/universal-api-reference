# Giftbit: Create Campaign Order

Creates a Giftbit campaign order for emailed or shortlink rewards.

```
POST https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/create-campaign-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Giftbit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/create-campaign-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "priceInCents": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/giftbit/latest/actions/create-campaign-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "priceInCents": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `giftTemplate` | string | no |  |
| `message` | string | no |  |
| `subject` | string | no |  |
| `contacts[].email` | string | no |  |
| `contacts[].firstname` | string | no |  |
| `contacts[].lastname` | string | no |  |
| `priceInCents` | number | yes |  |
| `brandCodes[]` | array<string> | no |  |
| `region` | string | no |  |
| `expiry` | date | no |  |
| `deliveryType` | string | no |  |
| `linkCount` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign": {},
      "info": {},
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign` | object |  |
| `info` | object |  |
| `status` | number |  |

## Native endpoint

Through the native Giftbit API, this operation is `POST /campaign` (base URL `https://api-testbed.giftbit.com/papi/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-campaign-order.md) for the provider-specific parameters and requirements.

