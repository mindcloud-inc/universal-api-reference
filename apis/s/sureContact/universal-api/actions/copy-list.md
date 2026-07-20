# SureContact: Copy List

Creates a copy of an existing SureContact list.

```
POST https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/copy-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SureContact `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/copy-list" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listUuid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sureContact/latest/actions/copy-list', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listUuid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `listUuid` | string | yes | The UUID of the list. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_count": 1,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "is_system": true,
      "name": "Ava Chen",
      "type": "string",
      "type_label": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_count` | number |  |
| `created_at` | date |  |
| `description` | string |  |
| `is_system` | boolean |  |
| `name` | string |  |
| `type` | string |  |
| `type_label` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native SureContact API, this operation is `POST api/v1/public/lists/:list_uuid/copy` (base URL `https://api.surecontact.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-list.md) for the provider-specific parameters and requirements.

