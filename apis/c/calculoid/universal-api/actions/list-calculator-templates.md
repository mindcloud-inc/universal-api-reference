# Calculoid: List Calculator Templates



```
GET https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-calculator-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Calculoid `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-calculator-templates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/calculoid/latest/actions/list-calculator-templates?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "calcs": [
        {
          "author": true,
          "authorName": "Ava Chen",
          "can": {
            "copy": true,
            "delete": true,
            "edit": true
          },
          "created": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "finished": "string",
          "id": "string",
          "language": "string",
          "modified": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "private": "string",
          "rating": "string",
          "ratingCount": "string",
          "tags": [
            "string"
          ],
          "username": "Ava Chen"
        }
      ],
      "pg": {
        "current": 1,
        "limit": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `calcs[].author` | boolean |  |
| `calcs[].authorName` | string |  |
| `calcs[].can.copy` | boolean |  |
| `calcs[].can.delete` | boolean |  |
| `calcs[].can.edit` | boolean |  |
| `calcs[].created` | date |  |
| `calcs[].description` | string |  |
| `calcs[].finished` | string |  |
| `calcs[].id` | string |  |
| `calcs[].language` | string |  |
| `calcs[].modified` | date |  |
| `calcs[].name` | string |  |
| `calcs[].private` | string |  |
| `calcs[].rating` | string |  |
| `calcs[].ratingCount` | string |  |
| `calcs[].tags[]` | string |  |
| `calcs[].username` | string |  |
| `pg.current` | number |  |
| `pg.limit` | number |  |
| `pg.total` | number |  |

## Native endpoint

Through the native Calculoid API, this operation is `GET /calculators/templates` (base URL `https://api.calculoid.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-calculator-templates.md) for the provider-specific parameters and requirements.

