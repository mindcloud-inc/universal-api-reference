# Documently: Retrieve Invitation

Retrieves an invitation from Documently.

```
GET https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-invitation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Documently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-invitation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/documently/latest/actions/retrieve-invitation?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invitationId` | string | no | The invitation id. |

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

Through the native Documently API, this operation is `GET /invitations/:invitationId` (base URL `https://app.documently.io/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-invitation.md) for the provider-specific parameters and requirements.

