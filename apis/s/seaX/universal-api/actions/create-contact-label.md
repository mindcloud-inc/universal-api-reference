# SeaX: Create Contact Label

Creates a contact label in the current SeaX workspace.

```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-contact-label
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-contact-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-contact-label', {
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
| `name` | string | yes | Contact label name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "color": "string",
      "created_time": "string",
      "description": "string",
      "id": "string",
      "is_system": true,
      "name": "Ava Chen",
      "updated_time": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created_time` | string |  |
| `description` | string |  |
| `id` | string |  |
| `is_system` | boolean |  |
| `name` | string |  |
| `updated_time` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /contact_labels` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact-label.md) for the provider-specific parameters and requirements.

