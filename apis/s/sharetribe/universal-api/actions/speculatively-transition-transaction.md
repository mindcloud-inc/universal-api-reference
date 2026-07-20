# Sharetribe: Speculatively Transition Transaction

Speculatively transitions a transaction in Sharetribe.

```
PUT https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/speculatively-transition-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sharetribe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/speculatively-transition-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "transition": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sharetribe/latest/actions/speculatively-transition-transaction', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "transition": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ID of the transaction. |
| `transition` | string | yes | The name of a possible next transition for the current transaction state. |
| `params` | object | no | Transition parameters object as required by the transaction process definition. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "relationships": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object | Resource attributes payload. |
| `id` | string | Resource ID. |
| `relationships` | object | Resource relationships payload. |
| `type` | string | Resource type. |

## Native endpoint

Through the native Sharetribe API, this operation is `POST transactions/transition_speculative` (base URL `https://flex-integ-api.sharetribe.com/v1/integration_api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/speculatively-transition-transaction.md) for the provider-specific parameters and requirements.

