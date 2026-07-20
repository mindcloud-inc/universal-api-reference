# CustomerX: List Contacts

Retrieves a list of contacts from CustomerX.

```
GET https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CustomerX `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/customerX/latest/actions/list-contacts?${params}`, {
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
      "birthday": "string",
      "client": {},
      "client_id": 1,
      "created_at": "string",
      "custom_attributes": [
        {}
      ],
      "email": "ava@example.com",
      "external_id_contact": "string",
      "id": 1,
      "is_principal": true,
      "name": "Ava Chen",
      "note": "string",
      "occupation": "string",
      "phones": [
        "string"
      ],
      "type_contact": {},
      "type_contact_id": 1,
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | string |  |
| `client` | object |  |
| `client_id` | number |  |
| `created_at` | string |  |
| `custom_attributes` | array<object> |  |
| `email` | string |  |
| `external_id_contact` | string |  |
| `id` | number |  |
| `is_principal` | boolean |  |
| `name` | string |  |
| `note` | string |  |
| `occupation` | string |  |
| `phones` | array<string> |  |
| `type_contact` | object |  |
| `type_contact_id` | number |  |
| `updated_at` | string |  |

## Native endpoint

Through the native CustomerX API, this operation is `GET /api/v1/contacts` (base URL `https://sandbox.api.customerx.com.br`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-contacts.md) for the provider-specific parameters and requirements.

