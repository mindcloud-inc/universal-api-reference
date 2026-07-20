# Octadesk: Create Contact

Creates a contact in Octadesk.

```
POST https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/create-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octadesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/create-contact" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "codex.octadesk.test@example.com",
  "name": "Codex Test Contact"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/create-contact', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "codex.octadesk.test@example.com",
    "name": "Codex Test Contact"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `email` | string | yes | Customer email. Example: `codex.octadesk.test@example.com`. |
| `name` | string | yes | Customer name. Example: `Codex Test Contact`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        "string"
      ],
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "organization": {
        "description": "string",
        "domains": [
          "string"
        ],
        "id": "string",
        "name": "Ava Chen"
      },
      "phoneContacts": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFields` | array |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `organization.description` | string |  |
| `organization.domains[]` | string |  |
| `organization.id` | string |  |
| `organization.name` | string |  |
| `phoneContacts` | array |  |

## Native endpoint

Through the native Octadesk API, this operation is `POST /contacts` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-contact.md) for the provider-specific parameters and requirements.

