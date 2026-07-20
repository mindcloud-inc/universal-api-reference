# Toofr: Create Email List Record

Creates a new email list record in Toofr.

```
POST https://connect.mindcloud.co/v1/universal/toofr/latest/actions/create-email-list-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/create-email-list-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "company": "string",
  "firstName": "Ava",
  "lastName": "Chen",
  "listId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toofr/latest/actions/create-email-list-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "company": "string",
    "firstName": "Ava",
    "lastName": "Chen",
    "listId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `company` | string | yes | Record company name. |
| `firstName` | string | yes | Record first name. |
| `lastName` | string | yes | Record last name. |
| `listId` | string | yes | Email list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "email_address": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "last_name": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `email_address` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `last_name` | string |  |

## Native endpoint

Through the native Toofr API, this operation is `POST /lists/:list_id/list_records` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-email-list-record.md) for the provider-specific parameters and requirements.

