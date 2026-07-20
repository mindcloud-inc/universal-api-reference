# Freshworks CRM: List Contacts

Retrieves contacts from a view in Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-contacts?${params}`, {
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
| `viewId` | number | no | Numeric view identifier used for list queries. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contacts": [
        {
          "city": "string",
          "country": "string",
          "created_at": "2026-05-07T12:00:00.000Z",
          "custom_field": {
            "cf_customer_id": "string"
          },
          "display_name": "Ava Chen",
          "email": "ava@example.com",
          "emails": [
            {
              "value": "ava@example.com"
            }
          ],
          "first_name": "Ava",
          "id": 1,
          "is_deleted": true,
          "last_name": "Chen",
          "lead_score": 1,
          "links": {
            "conversations": "https://example.com"
          },
          "mcr_id": 1,
          "mobile_number": "string",
          "updated_at": "2026-05-07T12:00:00.000Z"
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
| `contacts[].city` | string |  |
| `contacts[].country` | string |  |
| `contacts[].created_at` | date |  |
| `contacts[].custom_field.cf_customer_id` | string |  |
| `contacts[].display_name` | string |  |
| `contacts[].email` | string |  |
| `contacts[].emails[].value` | string |  |
| `contacts[].first_name` | string |  |
| `contacts[].id` | number |  |
| `contacts[].is_deleted` | boolean |  |
| `contacts[].last_name` | string |  |
| `contacts[].lead_score` | number |  |
| `contacts[].links.conversations` | string |  |
| `contacts[].mcr_id` | number |  |
| `contacts[].mobile_number` | string |  |
| `contacts[].updated_at` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET api/contacts/view/:view_id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

