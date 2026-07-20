# Pipedrive: Search Products

Finds products in Pipedrive by search term.

```
GET https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-products
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pipedrive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-products?connectionId=$CONNECTION_ID&limit=25&offset=0&term=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "term": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pipedrive/latest/actions/search-products?${params}`, {
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
| `term` | string | yes | Search term for products. |
| `exactMatch` | boolean | no | Set true to only return exact matches. |
| `limit` | number | no | Max number of results to return. |
| `cursor` | string | no | Pagination cursor from previous response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "items": [
        {
          "item": {
            "code": {},
            "id": 1,
            "name": "Ava Chen",
            "owner": {
              "id": 1
            },
            "tax": 1,
            "type": "string",
            "visibleTo": 1
          },
          "resultScore": 1
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
| `items[].item.code` | object |  |
| `items[].item.id` | number |  |
| `items[].item.name` | string |  |
| `items[].item.owner.id` | number |  |
| `items[].item.tax` | number |  |
| `items[].item.type` | string |  |
| `items[].item.visibleTo` | number |  |
| `items[].resultScore` | number |  |

## Native endpoint

Through the native Pipedrive API, this operation is `GET v2/products/search` (base URL `{{credentials.accessTokenRequest.api_domain}}/api`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-products.md) for the provider-specific parameters and requirements.

