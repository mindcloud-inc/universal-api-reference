# Tumblr: List Blog Following

Retrieves blogs followed by a Tumblr blog.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-blog-following
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-blog-following?connectionId=$CONNECTION_ID&limit=25&offset=0&blogIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "blogIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-blog-following?${params}`, {
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
| `blogIdentifier` | string | yes | The blog whose following list should be retrieved. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blogs": [
        {
          "canShowBadges": true,
          "description": "string",
          "name": "Ava Chen",
          "title": "string",
          "tumblrmartAccessories": {
            "badges": [
              {
                "destinationUrl": "https://example.com",
                "productGroup": "string",
                "urls": [
                  "https://example.com"
                ]
              }
            ],
            "blueCheckmarkCount": 1
          },
          "updated": 1,
          "url": "https://example.com",
          "uuid": "string"
        }
      ],
      "totalBlogs": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blogs[].canShowBadges` | boolean |  |
| `blogs[].description` | string |  |
| `blogs[].name` | string |  |
| `blogs[].title` | string |  |
| `blogs[].tumblrmartAccessories.badges[].destinationUrl` | string |  |
| `blogs[].tumblrmartAccessories.badges[].productGroup` | string |  |
| `blogs[].tumblrmartAccessories.badges[].urls[]` | string |  |
| `blogs[].tumblrmartAccessories.blueCheckmarkCount` | number |  |
| `blogs[].updated` | number |  |
| `blogs[].url` | string |  |
| `blogs[].uuid` | string |  |
| `totalBlogs` | number |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/following` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-blog-following.md) for the provider-specific parameters and requirements.

