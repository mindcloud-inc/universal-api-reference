# G2: List Categories

Retrieves categories from G2.

```
GET https://connect.mindcloud.co/v1/universal/g2/latest/actions/list-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a G2 `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/g2/latest/actions/list-categories?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/g2/latest/actions/list-categories?${params}`, {
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
| `fieldsCategories[]` | array<string> | no |  |
| `filterCreatedAtGt` | date | no |  |
| `filterCreatedAtLt` | date | no |  |
| `filterNameCont` | string | no |  |
| `filterNameEq` | string | no |  |
| `filterSlugCont` | string | no |  |
| `filterSlugEq` | string | no |  |
| `filterUpdatedAtGt` | date | no |  |
| `filterUpdatedAtLt` | date | no |  |
| `include[]` | array<string> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "description": "string",
        "name": "Ava Chen",
        "slug": "string",
        "updatedAt": "string",
        "uuid": "string"
      },
      "id": "string",
      "relationships": {
        "ancestors": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        },
        "parent": {
          "data": {
            "id": "string",
            "type": "string"
          }
        },
        "products": {
          "data": [
            {
              "id": "string",
              "type": "string"
            }
          ]
        }
      },
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.description` | string |  |
| `attributes.name` | string |  |
| `attributes.slug` | string |  |
| `attributes.updatedAt` | string |  |
| `attributes.uuid` | string |  |
| `id` | string |  |
| `relationships.ancestors.data[].id` | string |  |
| `relationships.ancestors.data[].type` | string |  |
| `relationships.parent.data.id` | string |  |
| `relationships.parent.data.type` | string |  |
| `relationships.products.data[].id` | string |  |
| `relationships.products.data[].type` | string |  |
| `type` | string |  |

## Native endpoint

Through the native G2 API, this operation is `GET /api/v2/categories` (base URL `https://data.g2.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-categories.md) for the provider-specific parameters and requirements.

