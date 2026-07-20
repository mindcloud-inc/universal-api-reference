# Edoobox: Create Offer

Creates a new offer in Edoobox.

```
POST https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/create-offer
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edoobox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/create-offer" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "string",
  "name": "Ava Chen",
  "number": "string",
  "type": "offer"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edoobox/latest/actions/create-offer', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "string",
    "name": "Ava Chen",
    "number": "string",
    "type": "offer"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | yes | Parent edoobox category ID for the new offer. |
| `name` | string | yes | Display name for the new offer. |
| `number` | string | yes | Unique offer number/code. |
| `type` | string | yes | edoobox offer type. Defaults to offer. Default: `offer`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "insert": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `insert` | boolean |  |

## Native endpoint

Through the native Edoobox API, this operation is `POST /offer` (base URL `https://app2.edoobox.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-offer.md) for the provider-specific parameters and requirements.

