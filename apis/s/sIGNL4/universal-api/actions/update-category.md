# SIGNL4: Update Category

Updates a category in SIGNL4.

```
PUT https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/update-category
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/update-category" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "teamId": "string",
  "categoryId": "string",
  "name": "Ava Chen",
  "color": "string",
  "imageName": "Ava Chen",
  "keywords[]": [
    "string"
  ],
  "keywordMatching": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/update-category', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "teamId": "string",
    "categoryId": "string",
    "name": "Ava Chen",
    "color": "string",
    "imageName": "Ava Chen",
    "keywords[]": ["string"],
    "keywordMatching": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `teamId` | string | yes | ID of the team the category belongs to |
| `categoryId` | string | yes |  |
| `name` | string | yes |  |
| `color` | string | yes |  |
| `imageName` | string | yes |  |
| `keywords[]` | array<string> | yes |  |
| `keywordMatching` | number | yes | <p/><ul><li>0 = Any</li><li>1 = All</li></ul> |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | no |  |
| `teamId` | string | no |  |
| `isDefault` | boolean | no |  |
| `options` | number | no | <p/><ul><li>0 = None</li><li>1 = Hidden</li><li>2 = DenyDelete</li><li>4 = HideOptOut</li><li>8 = HideKeywords</li></ul> |
| `keywordsExcluded[]` | array<string> | no |  |
| `augmentations[]` | array<object> | no |  |
| `enrichments[]` | array<object> | no |  |
| `order` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "augmentations": [
        {}
      ],
      "color": "string",
      "enrichments": {
        "id": "string",
        "name": "Ava Chen",
        "type": 1,
        "value": "string"
      },
      "id": "string",
      "imageName": "Ava Chen",
      "isDefault": true,
      "keywordMatching": 1,
      "keywords": [
        "string"
      ],
      "keywordsExcluded": [
        "string"
      ],
      "name": "Ava Chen",
      "options": 1,
      "order": 1,
      "teamId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `augmentations` | array<object> |  |
| `color` | string |  |
| `enrichments` | array<object> |  |
| `enrichments.id` | string |  |
| `enrichments.name` | string |  |
| `enrichments.type` | number |  |
| `enrichments.value` | string |  |
| `id` | string |  |
| `imageName` | string |  |
| `isDefault` | boolean |  |
| `keywordMatching` | number |  |
| `keywords` | array<string> |  |
| `keywordsExcluded` | array<string> |  |
| `name` | string |  |
| `options` | number |  |
| `order` | number |  |
| `teamId` | string |  |

## Native endpoint

Through the native SIGNL4 API, this operation is `PUT /v2/categories/{teamId}/{categoryId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-category.md) for the provider-specific parameters and requirements.

