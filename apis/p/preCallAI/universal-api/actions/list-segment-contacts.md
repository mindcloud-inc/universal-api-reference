# PreCallAI: List Segment Contacts

Retrieves segment contacts from PreCallAI.

```
GET https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-segment-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PreCallAI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-segment-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/preCallAI/latest/actions/list-segment-contacts?${params}`, {
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
| `id` | string | no | The segment ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": "string",
        "last_name": "Chen",
        "phone": "string"
      },
      "message": "string",
      "statistics": {
        "totalCallAnswered": 1,
        "totalCallPlaced": 1,
        "totalVoiceConsumed": 1
      },
      "status": 1,
      "success": true,
      "totalItems": 1,
      "totalPages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of segment contacts returned by PreCallAI. |
| `data.email` | string | Contact email address. |
| `data.first_name` | string | Contact first name. |
| `data.id` | string | Segment contact ID. |
| `data.last_name` | string | Contact last name. |
| `data.phone` | string | Contact phone number. |
| `message` | string | Provider status message for listing segment contacts. |
| `statistics` | object | Aggregate statistics for the segment contact list. |
| `statistics.totalCallAnswered` | number | Total calls answered for the segment. |
| `statistics.totalCallPlaced` | number | Total calls placed for the segment. |
| `statistics.totalVoiceConsumed` | number | Total voice consumed for the segment. |
| `status` | number | HTTP-style status returned by PreCallAI. |
| `success` | boolean | Whether the segment contacts list request succeeded. |
| `totalItems` | number | Total contacts returned for the segment. |
| `totalPages` | number | Total pages available for the segment contacts result. |

## Native endpoint

Through the native PreCallAI API, this operation is `GET /segment/contact/list` (base URL `https://api.precallai.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-segment-contacts.md) for the provider-specific parameters and requirements.

