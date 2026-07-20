# Spoki: List Templates

Lists templates for the authenticated account, with optional filtering by channel-specific WABA.

```
GET https://connect.mindcloud.co/v1/universal/spoki/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Spoki `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/spoki/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/spoki/latest/actions/list-templates?${params}`, {
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
| `search` | string | no | Search templates by id, name, or text. Example: `sale`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "category": "string",
      "customfieldSet": [
        "string"
      ],
      "id": 1,
      "integration": 1,
      "isApproved": true,
      "isFavorite": true,
      "name": "Ava Chen",
      "subcategory": "string",
      "templateGroups": [
        {}
      ],
      "templatelocalizationSet": [
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
| `category` | string |  |
| `customfieldSet` | array<string> |  |
| `id` | number |  |
| `integration` | number |  |
| `isApproved` | boolean |  |
| `isFavorite` | boolean |  |
| `name` | string |  |
| `subcategory` | string |  |
| `templateGroups` | array<object> |  |
| `templatelocalizationSet` | array<object> |  |

## Native endpoint

Through the native Spoki API, this operation is `GET /templates/` (base URL `https://api.spoki.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

