# Fruityvice: Get fruit by name



```
GET https://connect.mindcloud.co/v1/universal/fruityvice/latest/actions/get-fruit-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fruityvice `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fruityvice/latest/actions/get-fruit-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fruityvice/latest/actions/get-fruit-by-name?${params}`, {
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
| `name` | string | yes | Fruityvice fruit name. |

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

Through the native Fruityvice API, this operation is `GET /api/fruit/:name` (base URL `https://www.fruityvice.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-fruit-by-name.md) for the provider-specific parameters and requirements.

