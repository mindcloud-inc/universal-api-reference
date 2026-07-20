# Mode: Create Collection

Create a collection in a Mode workspace.

```
POST https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mode `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "space": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mode/latest/actions/create-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "space": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `space` | object | yes | Collection fields to create. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "defaultAccessLevel": "string",
      "description": "string",
      "Forms": {},
      "freeDefault": true,
      "id": "string",
      "Links": {},
      "name": "Ava Chen",
      "restricted": true,
      "schemaName": "Ava Chen",
      "spaceType": "string",
      "state": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `defaultAccessLevel` | string | Default collection access level. |
| `description` | string | Collection description. |
| `Forms` | object | Mode HAL forms. |
| `freeDefault` | boolean | Whether the collection is the free default collection. |
| `id` | string | Mode collection ID. |
| `Links` | object | Mode HAL links. |
| `name` | string | Collection name. |
| `restricted` | boolean | Whether the collection is restricted. |
| `schemaName` | string | Collection schema name. |
| `spaceType` | string | Collection type. |
| `state` | string | Collection state. |
| `token` | string | Mode collection token. |

## Native endpoint

Through the native Mode API, this operation is `POST /spaces` (base URL `https://app.mode.com/api/{{credentials.workspace}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-collection.md) for the provider-specific parameters and requirements.

