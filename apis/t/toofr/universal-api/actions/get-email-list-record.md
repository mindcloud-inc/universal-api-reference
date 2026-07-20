# Toofr: Get Email List Record

Retrieves an email list record from Toofr.

```
GET https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-email-list-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-email-list-record?connectionId=$CONNECTION_ID&id=string&listId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "listId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-email-list-record?${params}`, {
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
| `id` | string | yes | Email list record ID. |
| `listId` | string | yes | Email list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email_address": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen",
      "processed_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `created_at` | date |  |
| `email_address` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |
| `processed_at` | date |  |

## Native endpoint

Through the native Toofr API, this operation is `GET /lists/:list_id/list_records/:id` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-list-record.md) for the provider-specific parameters and requirements.

