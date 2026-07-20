# SuperSend: Get Contact

Retrieves a contact from SuperSend.

```
GET https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperSend `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superSend/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | Resource ID (UUID) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaign_id": "string",
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom": {},
      "deleted": true,
      "email": "ava@example.com",
      "finished": true,
      "first_name": "Ava",
      "id": "string",
      "interest": "string",
      "last_name": "Chen",
      "linkedin_url": "https://example.com",
      "phone": "string",
      "team_id": "string",
      "title": "string",
      "twitter": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "website": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaign_id` | string |  |
| `company` | string |  |
| `created_at` | date |  |
| `custom` | object |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `finished` | boolean |  |
| `first_name` | string |  |
| `id` | string |  |
| `interest` | string |  |
| `last_name` | string |  |
| `linkedin_url` | string |  |
| `phone` | string |  |
| `team_id` | string |  |
| `title` | string |  |
| `twitter` | string |  |
| `updated_at` | date |  |
| `website` | string |  |

## Native endpoint

Through the native SuperSend API, this operation is `GET /contacts/{id}` (base URL `https://api.supersend.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

