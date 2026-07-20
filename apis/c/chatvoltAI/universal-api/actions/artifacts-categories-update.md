# Chatvolt AI: Update Category

Updates a category in Chatvolt AI.

```
PUT https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-categories-update
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Chatvolt AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-categories-update" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/chatvoltAI/latest/actions/artifacts-categories-update', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `name` | string | no | Name for application/json requests. |
| `description` | string | no | Description for application/json requests. |
| `parentId` | string | no | ParentId for application/json requests. |
| `isActive` | boolean | no | IsActive for application/json requests. |

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

Through the native Chatvolt AI API, this operation is `PUT /artifact-categories/{id}` (base URL `https://api.chatvolt.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/artifacts-categories-update.md) for the provider-specific parameters and requirements.

