# Fruityvice: Get fruit by ID



```
GET https://connect.mindcloud.co/v1/universal/fruityvice/latest/actions/get-fruit-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fruityvice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fruityvice/latest/actions/get-fruit-by-id?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fruityvice/latest/actions/get-fruit-by-id?${params}`, {
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
| `id` | number | yes | Numeric Fruityvice fruit ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "family": "string",
      "genus": "string",
      "id": 1,
      "name": "Ava Chen",
      "nutritions": {},
      "order": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `family` | string | Botanical family. |
| `genus` | string | Botanical genus. |
| `id` | number | Fruityvice fruit identifier. |
| `name` | string | Fruit name. |
| `nutritions` | object | Nutrients per 100 grams. |
| `order` | string | Botanical order. |

## Native endpoint

Through the native Fruityvice API, this operation is `GET /api/fruit/:id` (base URL `https://www.fruityvice.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fruit-by-id.md) for the provider-specific parameters and requirements.

