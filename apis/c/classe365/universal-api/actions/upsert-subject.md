# Classe365: Upsert Subject

Creates or updates a subject in Classe365.

```
POST https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-subject
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Classe365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-subject" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/classe365/latest/actions/upsert-subject', {
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
| `code` | string | no | Subject code. |
| `name` | string | no | Subject name. |
| `section_id` | string | no | Section id. |
| `type` | string | no | Fixed value subject. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "classId": 1,
      "code": "string",
      "id": "string",
      "name": "Ava Chen",
      "sectionId": 1
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
| `sectionId` | number |  |

## Native endpoint

Through the native Classe365 API, this operation is `POST /rest/academic` (base URL `https://{{credentials.username}}.classe365.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-subject.md) for the provider-specific parameters and requirements.

