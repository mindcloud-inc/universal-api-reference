# Apideck: Create consumer

Creates a new consumer in Apideck Vault.

```
POST https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersadd
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apideck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersadd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "consumer_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apideck/latest/actions/consumersadd', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "consumer_id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `consumer_id` | string | yes |  |
| `metadata` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aggregated_request_count": 1,
      "application_id": "string",
      "connections": [
        {}
      ],
      "consumer_id": "string",
      "created": "string",
      "metadata": {},
      "modified": "string",
      "request_count_updated": "string",
      "request_counts": {},
      "services": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `aggregated_request_count` | number |  |
| `application_id` | string |  |
| `connections` | array<object> |  |
| `consumer_id` | string |  |
| `created` | string |  |
| `metadata` | object |  |
| `modified` | string |  |
| `request_count_updated` | string |  |
| `request_counts` | object |  |
| `services` | array<string> |  |

## Native endpoint

Through the native Apideck API, this operation is `POST /vault/consumers` (base URL `https://unify.apideck.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/consumersadd.md) for the provider-specific parameters and requirements.

