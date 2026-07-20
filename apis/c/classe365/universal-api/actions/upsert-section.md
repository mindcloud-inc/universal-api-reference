# Classe365: Upsert Section

Creates or updates a section in Classe365.

```
POST https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-section
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-section" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-section', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `class_id` | string | no | Class id. |
| `code` | string | no | Section code. |
| `name` | string | no | Section name. |
| `type` | string | no | Fixed value section. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classId": 1,
      "code": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `classId` | number |  |
| `code` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/academic` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-section.md) for the provider-specific parameters and requirements.

