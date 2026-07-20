# SurveySparrow: List Contacts

Retrieves all contacts from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-contacts?${params}`, {
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
| `type` | list | no | Filter contacts by delivery status. One of: `0`, `1`, `2`. |
| `search` | string | no | Search all contact properties for a matching value. |
| `contactType` | list | no | Filter by contact type. One of: `0`, `1`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contactListId` | number | no | Filter contacts by contact list ID. |
| `createdDateGte` | date | no | Return contacts created on or after this date. |
| `createdDateLte` | date | no | Return contacts created on or before this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "active": true,
      "contact_lists": [
        "string"
      ],
      "contact_type": "string",
      "created_at": {},
      "createddate": {},
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": 1,
      "job_title": "string",
      "last_name": "Chen",
      "mobile": "string",
      "name": "Ava Chen",
      "preferred_channels": [
        "string"
      ],
      "unsubscribe_text": "string",
      "unsubscribed": true,
      "unsubscribed_at": "string"
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
| `contact_lists` | array<string> |  |
| `contact_type` | string |  |
| `created_at` | object |  |
| `createddate` | object |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | number |  |
| `job_title` | string |  |
| `last_name` | string |  |
| `mobile` | string |  |
| `name` | string |  |
| `preferred_channels` | array<string> |  |
| `unsubscribe_text` | string |  |
| `unsubscribed` | boolean |  |
| `unsubscribed_at` | string |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /contacts` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

