# Parklio: Update Lot Description

Updates a lot description in Parklio.

```
PUT https://connect.mindcloud.co/v1/universal/parklio/latest/actions/update-lot-description
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parklio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/parklio/latest/actions/update-lot-description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parklio/latest/actions/update-lot-description', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The Parklio lot ID. |
| `description` | string | yes | The new lot description to apply. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Parklio API returns.

## Native endpoint

Through the native Parklio API, this operation is `PATCH /v2/lots/:id` (base URL `https://api.parklio.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-lot-description.md) for the provider-specific parameters and requirements.

