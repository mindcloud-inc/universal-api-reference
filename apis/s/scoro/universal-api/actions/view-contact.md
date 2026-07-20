# Scoro: View Contact

Retrieves contact details from Scoro.

```
GET https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scoro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scoro/latest/actions/view-contact?${params}`, {
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
| `id` | string | no | Scoro contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "client_profile_id": 1,
      "contact_id": 1,
      "contact_picture": "string",
      "contact_type": "string",
      "created_date": "string",
      "is_client": 1,
      "is_deleted": 1,
      "is_supplier": 1,
      "lastname": "Chen",
      "manager_email": "ava@example.com",
      "manager_id": 1,
      "means_of_contact": {},
      "modified_date": "string",
      "name": "Ava Chen",
      "search_name": "Ava Chen",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> |  |
| `client_profile_id` | number |  |
| `contact_id` | number |  |
| `contact_picture` | string |  |
| `contact_type` | string |  |
| `created_date` | string |  |
| `is_client` | number |  |
| `is_deleted` | number |  |
| `is_supplier` | number |  |
| `lastname` | string |  |
| `manager_email` | string |  |
| `manager_id` | number |  |
| `means_of_contact` | object |  |
| `modified_date` | string |  |
| `name` | string |  |
| `search_name` | string |  |
| `tags` | array<string> |  |

## Native endpoint

Through the native Scoro API, this operation is `POST contacts/view/:id` (base URL `{{credentials.subdomain}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/view-contact.md) for the provider-specific parameters and requirements.

