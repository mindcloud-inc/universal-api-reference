# Nyckel: Create Function

Creates a new function in Nyckel.

```
POST https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-function
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nyckel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-function" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "input": "string",
  "output": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nyckel/latest/actions/create-function', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "input": "string",
    "output": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | no | Human-readable function name. |
| `input` | string | yes | Input type for the function. |
| `output` | string | yes | Output type for the function. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "input": "string",
      "name": "Ava Chen",
      "output": "string",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `input` | string |  |
| `name` | string |  |
| `output` | string |  |
| `projectId` | string |  |

## Native endpoint

Through the native Nyckel API, this operation is `POST /functions` (base URL `https://www.nyckel.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-function.md) for the provider-specific parameters and requirements.

