# Octadesk: Get Contact

Retrieves a contact from Octadesk by ID.

```
GET https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Octadesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=fdaf98b3-9e64-4eb0-bd14-1771c936ed19" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "fdaf98b3-9e64-4eb0-bd14-1771c936ed19"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/octadesk/latest/actions/get-contact?${params}`, {
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
| `id` | string | yes | Contact ID from Octadesk. Example: `fdaf98b3-9e64-4eb0-bd14-1771c936ed19`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFields": [
        "string"
      ],
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "phoneContacts": [
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
| `customFields` | array |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `phoneContacts` | array |  |

## Native endpoint

Through the native Octadesk API, this operation is `GET /contacts/:id` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

