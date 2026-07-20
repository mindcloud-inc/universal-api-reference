# ProdPad: Get Company

Retrieves a company from ProdPad.

```
GET https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/get-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ProdPad `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/get-company?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/prodPad/latest/actions/get-company?${params}`, {
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
| `id` | string | yes | UUID of the company to fetch. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "size": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string |  |
| `country` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `name` | string |  |
| `size` | string |  |
| `updated_at` | date |  |
| `value` | string |  |

## Native endpoint

Through the native ProdPad API, this operation is `GET /companies/:id` (base URL `https://api.prodpad.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company.md) for the provider-specific parameters and requirements.

