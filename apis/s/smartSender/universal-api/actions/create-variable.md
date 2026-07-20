# Smart Sender: Create Variable

Creates a new variable in Smart Sender.

```
POST https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/create-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smart Sender `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/create-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/smartSender/latest/actions/create-variable', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional variable description. |
| `name` | string | yes | Unique variable name within the project. |
| `type` | string | yes | Variable type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": {},
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | object | Variable content definition returned by Smart Sender. |
| `createdAt` | date | Variable creation timestamp. |
| `description` | string | Variable description. |
| `id` | number | Smart Sender variable ID. |
| `name` | string | Variable name. |
| `updatedAt` | date | Variable last update timestamp. |
| `value` | string | Current variable value. |

## Native endpoint

Through the native Smart Sender API, this operation is `POST /v1/variables` (base URL `https://api.smartsender.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-variable.md) for the provider-specific parameters and requirements.

