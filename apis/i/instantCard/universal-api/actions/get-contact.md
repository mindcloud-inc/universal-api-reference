# InstantCard: Get Contact

Retrieves a contact from InstantCard by ID.

```
GET https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-contact
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InstantCard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-contact?connectionId=$CONNECTION_ID&id=1&organizationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "organizationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instantCard/latest/actions/get-contact?${params}`, {
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
| `id` | number | yes | Contact ID from InstantCard. |
| `organizationId` | number | yes | Organization ID from InstantCard. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addresses": [
        {}
      ],
      "alt_email": "ava@example.com",
      "alt_phone_number": "string",
      "email": "ava@example.com",
      "full_name": "Ava Chen",
      "id": 1,
      "organization_id": 1,
      "phone_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addresses` | array<object> | Related addresses. |
| `alt_email` | string | Alternate email address. |
| `alt_phone_number` | string | Alternate phone number. |
| `email` | string | Primary email address. |
| `full_name` | string | Contact full name. |
| `id` | number | Contact ID. |
| `organization_id` | number | Organization ID. |
| `phone_number` | string | Primary phone number. |

## Native endpoint

Through the native InstantCard API, this operation is `GET /api/v2/organizations/:organizationId/contacts/:id` (base URL `https://core.instantcard.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-contact.md) for the provider-specific parameters and requirements.

