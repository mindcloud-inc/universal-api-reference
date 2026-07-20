# Zapier NLA: List Guided Recipes



```
GET https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/list-guided-recipes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zapier NLA `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/list-guided-recipes?connectionId=$CONNECTION_ID&tags%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "tags[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapierNLA/latest/actions/list-guided-recipes?${params}`, {
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
| `query` | string | no | Optional search term for guided recipe suggestions. |
| `count` | number | no | Maximum number of guided recipes to return. Default: `5`. |
| `tags[]` | array<string> | yes | Tags used by Zapier to suggest relevant guided recipes. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "name": "Ava Chen",
      "results": [
        {}
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `name` | string |  |
| `results` | array<object> |  |
| `url` | string |  |

## Native endpoint

Through the native Zapier NLA API, this operation is `GET /api/v1/search/zaps/` (base URL `https://actions.zapier.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-guided-recipes.md) for the provider-specific parameters and requirements.

