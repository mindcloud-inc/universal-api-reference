# Toofr: List Marketplace Email Lists

Retrieves marketplace email lists from Toofr.

```
GET https://connect.mindcloud.co/v1/universal/toofr/latest/actions/list-marketplace-email-lists
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Toofr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toofr/latest/actions/list-marketplace-email-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toofr/latest/actions/list-marketplace-email-lists?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `page` | number | no | Optional provider page number. |

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

Through the native Toofr API, this operation is `GET /lists` (base URL `https://www.findemails.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-marketplace-email-lists.md) for the provider-specific parameters and requirements.

