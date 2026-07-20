# Chatvolt AI: Create Category

Creates a category in Chatvolt AI.

```
POST https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-categories-create
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-categories-create" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-categories-create', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Name for application/json requests. |
| `description` | string | no | Description for application/json requests. |
| `parentId` | string | no | ParentId for application/json requests. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "children": [
        "string"
      ],
      "description": "string",
      "id": "string",
      "isActive": true,
      "name": "Ava Chen",
      "parentId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `children` | array | Children. |
| `description` | string | Description. |
| `id` | string | Id. |
| `isActive` | boolean | IsActive. |
| `name` | string | Name. |
| `parentId` | string | ParentId. |

## Native endpoint

Through the native Chatvolt AI API, this operation is `POST /artifact-categories` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/artifacts-categories-create.md) for the provider-specific parameters and requirements.

