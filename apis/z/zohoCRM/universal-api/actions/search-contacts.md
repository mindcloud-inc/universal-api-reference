# Zoho CRM: Search Contacts

Finds contact records in Zoho CRM by search criteria.

```
GET https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/search-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/search-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/search-contacts?${params}`, {
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
| `criteria` | string | no | Use Zoho criteria syntax. Provide one of Criteria, Email, Phone, or Word. Example: `(Last_Name:equals:Burns)`. |
| `word` | string | no | Search by a free-text word. Provide one of Criteria, Email, Phone, or Word. Example: `Patricia`. |
| `email` | string | no | Search by an exact email address. Provide one of Criteria, Email, Phone, or Word. Example: `patricia@zylker.com`. |
| `phone` | string | no | Search by an exact phone number. Provide one of Criteria, Email, Phone, or Word. Example: `+1 555 555 5555`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields` | string | no | Comma-separated API names of fields to include in the response. Example: `Last_Name,Email,Full_Name`. |
| `converted` | boolean | no | Whether to include converted records in the result. |
| `approved` | boolean | no | Whether to restrict the result to approved records. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "id": "string",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `fullName` | string |  |
| `id` | string |  |
| `phone` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `GET /Contacts/search` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-contacts.md) for the provider-specific parameters and requirements.

