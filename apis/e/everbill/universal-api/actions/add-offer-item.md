# Everbill: Add Offer Item

Creates a new offer item in Everbill.

```
POST https://connect.mindcloud.co/v1/universal/everbill/latest/actions/add-offer-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Everbill `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/everbill/latest/actions/add-offer-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/everbill/latest/actions/add-offer-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Everbill record ID. |
| `article_id` | number | no | article_id request body field. |
| `new` | boolean | no | new request body field. |
| `name` | string | no | name request body field. |
| `quantity` | number | no | quantity request body field. |
| `description` | string | no | description request body field. |
| `unit` | string | no | unit request body field. |
| `price` | number | no | price request body field. |
| `ust` | number | no | ust request body field. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Everbill API returns.

## Native endpoint

Through the native Everbill API, this operation is `POST /offers/add_item/:id` (base URL `https://api.everbill.eu`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-offer-item.md) for the provider-specific parameters and requirements.

