# Simplecast: Get Podcast Subcategory

Retrieves a podcast subcategory from Simplecast by ID.

```
GET https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-podcast-subcategory
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simplecast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-podcast-subcategory?connectionId=$CONNECTION_ID&categoryId=string&podcastId=string&subcategoryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "categoryId": "string",
  "podcastId": "string",
  "subcategoryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simplecast/latest/actions/get-podcast-subcategory?${params}`, {
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
| `categoryId` | string | yes | Simplecast category identifier. |
| `podcastId` | string | yes | Simplecast podcast identifier. |
| `subcategoryId` | string | yes | Simplecast subcategory identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "collection": [
        {}
      ],
      "href": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `collection` | array<object> |  |
| `href` | string |  |
| `id` | string |  |

## Native endpoint

Through the native Simplecast API, this operation is `GET /podcasts/:podcast_id/categories/:category_id/subcategories/:subcategory_id` (base URL `https://api.simplecast.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-podcast-subcategory.md) for the provider-specific parameters and requirements.

