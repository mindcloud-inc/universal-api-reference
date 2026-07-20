# Documently: Create Invitation

Creates a new invitation in Documently.

```
POST https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-invitation" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/documently/latest/actions/create-invitation', {
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
| `email` | string | no | Invitee email. |
| `firstname` | string | no | Invitee first name. |
| `lastname` | string | no | Invitee last name. |
| `organization` | string | no | Organization IRI. |
| `project` | string | no | Project IRI. |
| `role` | string | no | Invitation role. |
| `status` | string | no | Invitation status. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "@context": "string",
      "@id": "string",
      "@type": "string",
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": "string",
      "lastname": "Chen",
      "organization": "string",
      "project": "string",
      "role": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `@context` | string |  |
| `@id` | string |  |
| `@type` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `id` | string |  |
| `lastname` | string |  |
| `organization` | string |  |
| `project` | string |  |
| `role` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Documently API, this operation is `POST /invitations` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-invitation.md) for the provider-specific parameters and requirements.

