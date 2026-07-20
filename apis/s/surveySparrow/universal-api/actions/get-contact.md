# SurveySparrow: Get Contact

Retrieves a contact from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | ID of the contact. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "active": true,
      "contact_lists": [
        {}
      ],
      "contact_type": "string",
      "created_at": {},
      "createddate": {},
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "job_title": {},
      "last_name": "Chen",
      "mobile": {},
      "name": "Ava Chen",
      "preferred_channels": [
        {}
      ],
      "unique_id": "string",
      "unsubscribe_text": {},
      "unsubscribed": true,
      "unsubscribed_at": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `active` | boolean |  |
| `contact_lists` | array<object> |  |
| `contact_type` | string |  |
| `created_at` | object |  |
| `createddate` | object |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `job_title` | object |  |
| `last_name` | string |  |
| `mobile` | object |  |
| `name` | string |  |
| `preferred_channels` | array<object> |  |
| `unique_id` | string |  |
| `unsubscribe_text` | object |  |
| `unsubscribed` | boolean |  |
| `unsubscribed_at` | object |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /contacts/{{id}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

