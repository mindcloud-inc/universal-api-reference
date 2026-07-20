# SeaX: Create Contact

Creates a contact in the current SeaX workspace.

```
POST https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeaX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seaX/latest/actions/create-contact', {
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
| `name` | string | yes | Contact name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_labels": [
        {}
      ],
      "created_time": "string",
      "id": "string",
      "name": "Ava Chen",
      "note": "string",
      "phone": "string",
      "updated_time": "string",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_labels` | array<object> |  |
| `created_time` | string |  |
| `id` | string |  |
| `name` | string |  |
| `note` | string |  |
| `phone` | string |  |
| `updated_time` | string |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native SeaX API, this operation is `POST /contacts` (base URL `https://seax.seasalt.ai/seax-api/api/v1/workspace/{{credentials.workspaceId}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

