# InflatableOffice: List Categories By Location

Retrieves categories for a location from InflatableOffice.

```
GET https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-categories-by-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a InflatableOffice `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-categories-by-location?connectionId=$CONNECTION_ID&limit=25&offset=0&locationId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "locationId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inflatableOffice/latest/actions/list-categories-by-location?${params}`, {
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
| `locationId` | number | yes | Location ID to filter categories for a specific location. Example: `0`. |

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
      "locationId": "string",
      "name": "Ava Chen",
      "order": "string",
      "wordpressUrls": [
        {
          "relativeUrl": "https://example.com",
          "website": "https://example.com"
        }
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
| `locationId` | string |  |
| `name` | string |  |
| `order` | string |  |
| `wordpressUrls[].relativeUrl` | string |  |
| `wordpressUrls[].website` | string |  |

## Native endpoint

Through the native InflatableOffice API, this operation is `GET /categories_list` (base URL `https://rental.software/api6`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-categories-by-location.md) for the provider-specific parameters and requirements.

