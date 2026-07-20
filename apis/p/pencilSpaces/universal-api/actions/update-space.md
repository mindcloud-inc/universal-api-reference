# Pencil Spaces: Update Space



```
PUT https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/update-space
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pencil Spaces `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/update-space" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "spaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pencilSpaces/latest/actions/update-space', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "spaceId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `space` | object | no | Container for mutable Space fields. |
| `space.archived` | boolean | no | Whether the Space should be archived. |
| `space.title` | string | no | Updated title for the Space. |
| `space.visibility` | string | no | Updated visibility for the Space. |
| `spaceId` | string | yes | The Pencil spaceId of the Space to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pencil Spaces API returns.

## Native endpoint

Through the native Pencil Spaces API, this operation is `PATCH /spaces/:spaceId` (base URL `https://apis.pencilapp.com/public/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-space.md) for the provider-specific parameters and requirements.

