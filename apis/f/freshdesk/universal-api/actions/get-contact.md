# Freshdesk: Get Contact

Retrieves a contact from Freshdesk by ID.

```
GET https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshdesk `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshdesk/latest/actions/get-contact?${params}`, {
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
| `id` | list<number> | yes | Freshdesk contact ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "companyId": 1,
      "contactType": "string",
      "createdAt": "string",
      "deleted": true,
      "email": "ava@example.com",
      "id": 1,
      "mobile": "string",
      "name": "Ava Chen",
      "phone": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `companyId` | number |  |
| `contactType` | string |  |
| `createdAt` | string |  |
| `deleted` | boolean |  |
| `email` | string |  |
| `id` | number |  |
| `mobile` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `updatedAt` | string |  |

## Native endpoint

Through the native Freshdesk API, this operation is `GET /contacts/:id` (base URL `https://{{credentials.subdomain}}.freshdesk.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

