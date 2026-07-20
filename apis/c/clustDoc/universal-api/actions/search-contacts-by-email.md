# ClustDoc: Search Contacts By Email



```
GET https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-contacts-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClustDoc `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-contacts-by-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "email": "ava@example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clustDoc/latest/actions/search-contacts-by-email?${params}`, {
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
| `email` | string | yes | Contact email address to match. |

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

Through the native ClustDoc API, this operation is `GET /contacts` (base URL `https://api.clustdoc.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-contacts-by-email.md) for the provider-specific parameters and requirements.

