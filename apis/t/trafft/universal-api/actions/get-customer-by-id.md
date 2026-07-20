# Trafft: Get Customer by ID

Retrieves a customer from Trafft by ID.

```
GET https://connect.mindcloud.co/v1/universal/trafft/latest/actions/get-customer-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trafft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trafft/latest/actions/get-customer-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trafft/latest/actions/get-customer-by-id?${params}`, {
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
| `id` | number | yes | The Trafft customer ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "birthday": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "gender": "string",
      "id": 1,
      "last_name": "Chen",
      "phone_country_code": "string",
      "phone_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `birthday` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `gender` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `phone_country_code` | string |  |
| `phone_number` | string |  |

## Native endpoint

Through the native Trafft API, this operation is `GET /customers/:id` (base URL `https://mindcloud.admin.trafft.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-customer-by-id.md) for the provider-specific parameters and requirements.

