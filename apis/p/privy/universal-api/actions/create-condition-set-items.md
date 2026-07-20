# Privy: Create Condition Set Items

Creates items in a Privy condition set.

```
POST https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-condition-set-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-condition-set-items" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "conditionSetId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-condition-set-items', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "conditionSetId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `conditionSetId` | string | yes | Privy condition set ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "condition_set_id": "string",
      "created_at": 1,
      "id": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `condition_set_id` | string |  |
| `created_at` | number |  |
| `id` | string |  |
| `value` | string |  |

## Native endpoint

Through the native Privy API, this operation is `POST /v1/condition_sets/{{conditionSetId}}/condition_set_items` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-condition-set-items.md) for the provider-specific parameters and requirements.

