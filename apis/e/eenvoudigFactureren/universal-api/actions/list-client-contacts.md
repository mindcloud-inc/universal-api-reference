# EenvoudigFactureren: List Client Contacts

Retrieves client contacts from EenvoudigFactureren.

```
GET https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-client-contacts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EenvoudigFactureren `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-client-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0&client_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "client_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eenvoudigFactureren/latest/actions/list-client-contacts?${params}`, {
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
| `client_id` | string | yes | EenvoudigFactureren client ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "contact_id": 1,
      "contact_name": "Ava Chen",
      "email_address": "ava@example.com",
      "phone_number": "string",
      "uri": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `contact_id` | number |  |
| `contact_name` | string |  |
| `email_address` | string |  |
| `phone_number` | string |  |
| `uri` | string |  |

## Native endpoint

Through the native EenvoudigFactureren API, this operation is `GET /clients/:client_id/contacts` (base URL `https://eenvoudigfactureren.be/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-client-contacts.md) for the provider-specific parameters and requirements.

