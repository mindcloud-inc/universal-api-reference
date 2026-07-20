# Magileads: List Contact List Contacts

Retrieves contacts from a Magileads contact list.

```
GET https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-contact-list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Magileads `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-contact-list-contacts?connectionId=$CONNECTION_ID&contact_list_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contact_list_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/magileads/latest/actions/list-contact-list-contacts?${params}`, {
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
| `contact_list_id` | number | yes | The contact list ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": "string",
      "next_page": "string",
      "number_of_contacts": 1,
      "number_of_emails": 1,
      "number_of_linkedin_url": 1,
      "number_of_pages": 1,
      "number_of_results": 1,
      "previous_page": "string",
      "results": [
        {}
      ],
      "state": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | string |  |
| `next_page` | string |  |
| `number_of_contacts` | number |  |
| `number_of_emails` | number |  |
| `number_of_linkedin_url` | number |  |
| `number_of_pages` | number |  |
| `number_of_results` | number |  |
| `previous_page` | string |  |
| `results` | array<object> |  |
| `state` | boolean |  |

## Native endpoint

Through the native Magileads API, this operation is `GET /contact-lists/:contact_list_id/contacts` (base URL `https://app.api-magileads.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contact-list-contacts.md) for the provider-specific parameters and requirements.

