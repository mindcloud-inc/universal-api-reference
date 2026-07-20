# Fiserv: Refund Adhoc Fee

Creates a refund for an adhoc fee in Fiserv.

```
POST https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/refund-adhoc-fee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fiserv `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/refund-adhoc-fee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "amount": 1,
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fiserv/latest/actions/refund-adhoc-fee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "amount": 1,
    "description": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Fee ID to refund. |
| `amount` | number | yes | Refund amount in minor units. |
| `description` | string | yes | Refund description. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `referenceId` | string | no | Optional external reference ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Fiserv API returns.

## Native endpoint

Through the native Fiserv API, this operation is `POST /fees/:id/refund` (base URL `https://bankinghub-cert.fiservapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/refund-adhoc-fee.md) for the provider-specific parameters and requirements.

