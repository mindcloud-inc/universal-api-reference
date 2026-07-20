# Goodbarber eCommerce: List Tags



```
GET https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-tags
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Goodbarber eCommerce `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-tags?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/goodbarberECommerce/latest/actions/list-tags?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sort` | string | no | Sorts the returned tags. Possible values: alpha : ascending alphabetical order last_created : descending creation date order most_tagged : sorted by descending number of products using this tag |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "next": "string",
      "previous": "string",
      "tags": [
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
| `count` | number | <div class="field_description">Number of tags returned by the API.</div> |
| `next` | string | <div class="field_description">URL to access the next page of the tags list.</div> |
| `previous` | string | <div class="field_description">URL to access the previous page of the tags list.</div> |
| `tags` | array<object> | <div class="field_description">List of tags.</div> |

## Native endpoint

Through the native Goodbarber eCommerce API, this operation is `GET /publicapi/v2/general/catalog/:webzine_id/tag/` (base URL `https://commerce.goodbarber.dev`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-tags.md) for the provider-specific parameters and requirements.

