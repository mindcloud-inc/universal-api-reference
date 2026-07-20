# InflatableOffice: List Categories

Retrieves categories from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-categories?${params}`, {
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
      "description": "string",
      "href": "string",
      "id": "string",
      "imageloc": "string",
      "imagelocbig": "string",
      "location_id": "string",
      "name": "Ava Chen",
      "order": "string",
      "requestTime": 1,
      "wordpress_urls": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `href` | string |  |
| `id` | string |  |
| `imageloc` | string |  |
| `imagelocbig` | string |  |
| `location_id` | string |  |
| `name` | string |  |
| `order` | string |  |
| `requestTime` | number |  |
| `wordpress_urls` | array<object> |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /categories_list` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

