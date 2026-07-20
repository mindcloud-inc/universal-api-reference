# SIGNL4: List Team Categories

Retrieves categories for a team from SIGNL4.

```
GET https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-team-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SIGNL4 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-team-categories?connectionId=$CONNECTION_ID&teamId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sIGNL4/latest/actions/list-team-categories?${params}`, {
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
| `teamId` | string | yes | ID of the team the categories belong to |

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

Through the native SIGNL4 API, this operation is `GET /v2/categories/{teamId}` (base URL `https://connect.signl4.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-categories.md) for the provider-specific parameters and requirements.

