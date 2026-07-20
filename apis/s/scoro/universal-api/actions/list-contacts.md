# Scoro: List Contacts

Retrieves contacts from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/list-contacts?${params}`, {
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
      "addresses": {},
      "bankaccount": "string",
      "birthday": {},
      "cat_id": 1,
      "client_profile_id": 1,
      "comments": "string",
      "contact_id": 1,
      "contact_picture": "string",
      "contact_type": "string",
      "created_date": "string",
      "deleted_date": {},
      "id_code": "string",
      "is_client": true,
      "is_deleted": true,
      "is_supplier": true,
      "lastname": "Chen",
      "manager_email": "ava@example.com",
      "manager_id": 1,
      "means_of_contact": {},
      "modified_date": "string",
      "name": "Ava Chen",
      "permissions": {},
      "position": "string",
      "reference_no": "string",
      "search_name": "Ava Chen",
      "sex": "string",
      "timezone": "string",
      "vatno": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | object | Address collection for the contact. |
| `bankaccount` | string | Bank account for the contact. |
| `birthday` | object | Birthday when available. |
| `cat_id` | number | Category ID. |
| `client_profile_id` | number | Client profile ID. |
| `comments` | string | Contact comments. |
| `contact_id` | number | Scoro contact ID. |
| `contact_picture` | string | Profile image URL. |
| `contact_type` | string | Contact type, such as person or company. |
| `created_date` | string | Created timestamp. |
| `deleted_date` | object | Deleted timestamp when the record is deleted. |
| `id_code` | string | Person or company identification code. |
| `is_client` | boolean | Whether the contact is marked as a client. |
| `is_deleted` | boolean | Whether the contact is deleted. |
| `is_supplier` | boolean | Whether the contact is marked as a supplier. |
| `lastname` | string | Contact last name for person records. |
| `manager_email` | string | Manager email. |
| `manager_id` | number | Manager user ID. |
| `means_of_contact` | object | Phone, website, mobile, and similar contact methods. |
| `modified_date` | string | Last modified timestamp. |
| `name` | string | Contact first name or company name. |
| `permissions` | object | Permissions payload when available. |
| `position` | string | Role or job title. |
| `reference_no` | string | Reference number. |
| `search_name` | string | Full contact name used for search. |
| `sex` | string | Gender marker when present. |
| `timezone` | string | Contact timezone. |
| `vatno` | string | VAT number. |

## Native endpoint

Through the native Scoro API, this operation is `POST contacts/list` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

