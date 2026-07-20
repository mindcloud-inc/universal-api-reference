# Wasi: Get Client

Retrieves a client from Wasi.

```
GET https://connect.mindcloud.co/v1/universal/wasi/latest/actions/get-client
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wasi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/get-client?connectionId=$CONNECTION_ID&client_id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "client_id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/get-client?${params}`, {
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
| `client_id` | number | yes | Wasi client ID to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "birthday": "2026-05-07T12:00:00.000Z",
      "cell_phone": "string",
      "city_label": "string",
      "client_origin_label": "string",
      "client_types": [
        {}
      ],
      "comment": "string",
      "country_label": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id_city": 1,
      "id_client": 1,
      "id_client_origin": 1,
      "id_client_status": 1,
      "id_country": 1,
      "id_region": 1,
      "id_user": 1,
      "identificacion": "string",
      "identification": "string",
      "last_name": "Chen",
      "phone": "string",
      "query": "string",
      "reference": "string",
      "region_label": "string",
      "send_information": true,
      "tag": [
        {}
      ],
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string | Client address. |
| `birthday` | date | Client birthday. |
| `cell_phone` | string | Client mobile phone number. |
| `city_label` | string | City name. |
| `client_origin_label` | string | Client origin label. |
| `client_types` | array<object> | Client type associations. |
| `comment` | string | Client comment. |
| `country_label` | string | Country name. |
| `created_at` | date | Client creation timestamp. |
| `email` | string | Client email address. |
| `first_name` | string | Client first name. |
| `id_city` | number | City identifier. |
| `id_client` | number | Wasi client identifier. |
| `id_client_origin` | number | Client origin identifier. |
| `id_client_status` | number | Client status identifier. |
| `id_country` | number | Country identifier. |
| `id_region` | number | Region identifier. |
| `id_user` | number | Assigned Wasi user identifier. |
| `identificacion` | string | Legacy Wasi identification field spelling. |
| `identification` | string | Client identification number. |
| `last_name` | string | Client last name. |
| `phone` | string | Client phone number. |
| `query` | string | Client search notes from Wasi. |
| `reference` | string | Client reference. |
| `region_label` | string | Region name. |
| `send_information` | boolean | Whether the client accepts information messages. |
| `tag` | array<object> | Client tags. |
| `updated_at` | date | Client update timestamp. |

## Native endpoint

Through the native Wasi API, this operation is `GET /client/get/:id_client` (base URL `https://api.wasi.co/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-client.md) for the provider-specific parameters and requirements.

