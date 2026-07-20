# BoxHero: List Partners

Retrieves partners from BoxHero.

```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-partners
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-partners?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/list-partners?${params}`, {
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
| `cursor` | number | no | Cursor for the next page of partners |
| `limit` | number | no | Maximum number of partners to return |
| `type` | number | no | Filter partners by type: supplier or customer |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "cursor": 1,
      "has_more": true,
      "items": [
        {
          "address": "string",
          "email": "ava@example.com",
          "id": 1,
          "memo": "string",
          "name": "Ava Chen",
          "phone": "string",
          "type": 1
        }
      ],
      "limit": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `cursor` | number |  |
| `has_more` | boolean |  |
| `items[].address` | string |  |
| `items[].email` | string |  |
| `items[].id` | number |  |
| `items[].memo` | string |  |
| `items[].name` | string |  |
| `items[].phone` | string |  |
| `items[].type` | number |  |
| `limit` | number |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/partners` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-partners.md) for the provider-specific parameters and requirements.

