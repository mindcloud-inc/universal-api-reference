# ClustDoc: List Contacts



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/list-contacts?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "company": "string",
      "company_id": 1,
      "display_name": "Ava Chen",
      "email": "ava@example.com",
      "firstname": "Ava",
      "full_name": "Ava Chen",
      "id": 1,
      "initials": "string",
      "lastname": "Chen",
      "phone": "string",
      "team_id": 1,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `company` | string |  |
| `company_id` | number |  |
| `display_name` | string |  |
| `email` | string |  |
| `firstname` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `initials` | string |  |
| `lastname` | string |  |
| `phone` | string |  |
| `team_id` | number |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ClustDoc API, this operation is `GET /contacts` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

