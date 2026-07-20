# Docutray: Update Knowledge Base



```
PUT https://connect.mindcloud.co/v1/universal/docutray/latest/actions/update-knowledge-base
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docutray `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docutray/latest/actions/update-knowledge-base" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docutray/latest/actions/update-knowledge-base', {
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
| `id` | string | yes | Unique ID of the Knowledge Base |
| `name` | string | no | New name for the knowledge base |
| `description` | string | no | New description for the knowledge base |
| `schema` | object | no | Updated JSON schema for documents |
| `indexingPreferences` | object | no | Updated indexing preferences |
| `isActive` | boolean | no | Active status of the knowledge base |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "indexingPreferences": {},
      "isActive": true,
      "name": "Ava Chen",
      "organizationId": "string",
      "schema": {},
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `description` | string |  |
| `id` | string |  |
| `indexingPreferences` | object |  |
| `isActive` | boolean |  |
| `name` | string |  |
| `organizationId` | string |  |
| `schema` | object |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Docutray API, this operation is `PUT api/knowledge-bases/:id` (base URL `https://app.docutray.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-knowledge-base.md) for the provider-specific parameters and requirements.

