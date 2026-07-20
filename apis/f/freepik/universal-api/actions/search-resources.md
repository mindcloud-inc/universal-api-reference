# Freepik: Search Resources

Finds Freepik resources by search term and filters.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-resources
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-resources?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/search-resources?${params}`, {
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
| `term` | string | no | Search term used to find Freepik resources. Example: `car`. |
| `order` | list | no | Search result ordering. Freepik supports relevance or recent. One of: `recent`, `relevance`. Default: `relevance`. |
| `limit` | number | no | Maximum number of resources to return. Default: `1`. |
| `page` | number | no | One-based results page to request. Default: `1`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "author": {},
      "filename": "Ava Chen",
      "id": 1,
      "image": {},
      "licenses": [
        {}
      ],
      "meta": {},
      "products": [
        {}
      ],
      "related": {},
      "stats": {},
      "title": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean | Whether the resource is active. |
| `author` | object | Resource author information. |
| `filename` | string | Download filename for the resource package. |
| `id` | number | Freepik resource ID. |
| `image` | object | Preview image metadata and source URL. |
| `licenses` | array<object> | License entries for the resource. |
| `meta` | object | Resource metadata, including publication and available format details. |
| `products` | array<object> | Product/license product entries associated with the resource. |
| `related` | object | Related resources and keyword metadata. |
| `stats` | object | Resource engagement statistics. |
| `title` | string | Resource title. |
| `url` | string | Freepik resource page URL. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/resources` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-resources.md) for the provider-specific parameters and requirements.

