# Wiza: Get List Contacts

Retrieves contacts for a Wiza list.

```
GET https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wiza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-list-contacts?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wiza/latest/actions/get-list-contacts?${params}`, {
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
| `id` | number | yes | ID of the list whose contacts to fetch. |
| `segment` | string | no | Optional list segment to return. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "company": "string",
          "company_domain": "string",
          "email": "ava@example.com",
          "email_status": "ava@example.com",
          "first_name": "Ava",
          "full_name": "Ava Chen",
          "last_name": "Chen",
          "linkedin": "https://example.com",
          "title": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Enriched contacts from the list. |
| `data[].company` | string | Company name. |
| `data[].company_domain` | string | Company domain. |
| `data[].email` | string | Primary email. |
| `data[].email_status` | string | Email verification status. |
| `data[].first_name` | string | Contact first name. |
| `data[].full_name` | string | Contact full name. |
| `data[].last_name` | string | Contact last name. |
| `data[].linkedin` | string | LinkedIn profile URL. |
| `data[].title` | string | Current title. |

## Native endpoint

Through the native Wiza API, this operation is `GET /lists/:id/contacts` (base URL `https://wiza.co/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-list-contacts.md) for the provider-specific parameters and requirements.

