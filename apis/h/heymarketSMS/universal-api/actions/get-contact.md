# Heymarket SMS: Get Contact



```
GET https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Heymarket SMS `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/heymarketSMS/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | Contact id to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assigned_user_id": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "creator_id": 1,
      "display_name": "Ava Chen",
      "email": "ava@example.com",
      "first": "string",
      "id": 1,
      "last": "string",
      "op": "string",
      "phone": "string",
      "rev": 1,
      "shared": true,
      "team_id": 1,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assigned_user_id` | number |  |
| `created` | date |  |
| `creator_id` | number |  |
| `display_name` | string |  |
| `email` | string |  |
| `first` | string |  |
| `id` | number |  |
| `last` | string |  |
| `op` | string |  |
| `phone` | string |  |
| `rev` | number |  |
| `shared` | boolean |  |
| `team_id` | number |  |
| `updated` | date |  |

## Native endpoint

Through the native Heymarket SMS API, this operation is `GET /v1/contact/:id` (base URL `https://api.heymarket.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

