# Claid AI: Create Storage

Creates a storage connector in Claid AI.

```
POST https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/create-storage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Claid AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/create-storage" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "parameters": {},
  "type": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/claidAI/latest/actions/create-storage', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "parameters": {},
    "type": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes |  |
| `parameters` | object | yes |  |
| `type` | string | yes | One of: `0`, `1`, `2`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "parameters": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number | Storage identifier. |
| `name` | string | Storage name in Claid. |
| `parameters` | object | Connector-specific storage parameters. |
| `type` | string | Storage connector type. |

## Native endpoint

Through the native Claid AI API, this operation is `POST storage/storages` (base URL `https://api.claid.ai/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-storage.md) for the provider-specific parameters and requirements.

