# Synthflow AI Phone Calling: Get Contact

Retrieves a contact from your Synthflow workspace.

```
GET https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Synthflow AI Phone Calling `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/get-contact?connectionId=$CONNECTION_ID&contactId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/synthflowAIPhoneCalling/latest/actions/get-contact?${params}`, {
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
| `contactId` | string | yes | The Synthflow contact identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_metadata": {},
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": "string",
      "memories": [
        {}
      ],
      "name": "Ava Chen",
      "phone_number": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "workspace_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_metadata` | object |  |
| `created_at` | date |  |
| `email` | string |  |
| `id` | string |  |
| `memories` | array<object> |  |
| `name` | string |  |
| `phone_number` | string |  |
| `updated_at` | date |  |
| `workspace_id` | string |  |

## Native endpoint

Through the native Synthflow AI Phone Calling API, this operation is `GET /contacts/:contact_id` (base URL `https://api.synthflow.ai/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

