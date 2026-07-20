# Toofr: Get Email List

Retrieves an email list from Toofr.

```
GET https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-email-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-email-list?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toofr/latest/actions/get-email-list?${params}`, {
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
| `id` | string | yes | Email list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "file_type": "string",
      "id": "string",
      "list_records_count": 1,
      "name": "Ava Chen",
      "records_count_in": 1,
      "records_count_processed": 1,
      "state": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `file_type` | string |  |
| `id` | string |  |
| `list_records_count` | number |  |
| `name` | string |  |
| `records_count_in` | number |  |
| `records_count_processed` | number |  |
| `state` | string |  |

## Native endpoint

Through the native Toofr API, this operation is `GET /lists/:id` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-email-list.md) for the provider-specific parameters and requirements.

