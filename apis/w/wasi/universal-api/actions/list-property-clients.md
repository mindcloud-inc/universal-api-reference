# Wasi: List Property Clients

Retrieves clients linked to a property in Wasi.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-property-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-property-clients?connectionId=$CONNECTION_ID&property_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "property_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-property-clients?${params}`, {
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
| `property_id` | number | yes | Wasi property ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "cell_phone": "string",
      "client_type_label": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id_client": 1,
      "id_client_type": 1,
      "last_name": "Chen",
      "phone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cell_phone` | string | Client mobile phone number. |
| `client_type_label` | string | Relationship client type label. |
| `email` | string | Client email address. |
| `first_name` | string | Client first name. |
| `id_client` | number | Related Wasi client identifier. |
| `id_client_type` | number | Relationship client type identifier. |
| `last_name` | string | Client last name. |
| `phone` | string | Client phone number. |

## Native endpoint

Through the native Wasi API, this operation is `GET /property/clients/:id_property` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-property-clients.md) for the provider-specific parameters and requirements.

