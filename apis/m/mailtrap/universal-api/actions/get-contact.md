# Mailtrap: Get Contact

Retrieves a contact from Mailtrap.

```
GET https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailtrap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/get-contact?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailtrap/latest/actions/get-contact?${params}`, {
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
      "data": {
        "createdAt": 1,
        "email": "ava@example.com",
        "fields": {
          "company": "string",
          "firstName": "Ava",
          "lastName": "Chen"
        },
        "id": "string",
        "listIds": [
          1
        ],
        "status": "string",
        "updatedAt": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createdAt` | number |  |
| `data.email` | string |  |
| `data.fields.company` | string |  |
| `data.fields.firstName` | string |  |
| `data.fields.lastName` | string |  |
| `data.id` | string |  |
| `data.listIds` | array<number> |  |
| `data.status` | string |  |
| `data.updatedAt` | number |  |

## Native endpoint

Through the native Mailtrap API, this operation is `GET /contacts/{contact_identifier}` (base URL `https://mailtrap.io/api/accounts/:account_id`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

