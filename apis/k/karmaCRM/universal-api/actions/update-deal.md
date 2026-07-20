# Karma CRM: Update Deal

Updates an existing deal in Karma CRM.

```
PUT https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/update-deal
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Karma CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/update-deal" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1,
  "deal": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/karmaCRM/latest/actions/update-deal', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1,
    "deal": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | The ID of the deal to update. |
| `deal` | object | yes | Deal payload object with the fields to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Karma CRM API returns.

## Native endpoint

Through the native Karma CRM API, this operation is `PUT /api/v3/deals/:id.json` (base URL `https://app.karmacrm.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-deal.md) for the provider-specific parameters and requirements.

