# Port API AI: Create Blueprint

Creates a blueprint in Port.

```
POST https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-blueprint
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Port API AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-blueprint" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "icon": "string",
  "identifier": "string",
  "schema": {},
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/portAPIAI/latest/actions/create-blueprint', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "icon": "string",
    "identifier": "string",
    "schema": {},
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `icon` | string | yes | Blueprint icon |
| `identifier` | string | yes | Blueprint identifier |
| `schema` | object | yes | Blueprint schema |
| `title` | string | yes | Blueprint title |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blueprint": {},
      "ok": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blueprint` | object |  |
| `ok` | boolean |  |

## Native endpoint

Through the native Port API AI API, this operation is `POST /blueprints` (base URL `https://api.port.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-blueprint.md) for the provider-specific parameters and requirements.

