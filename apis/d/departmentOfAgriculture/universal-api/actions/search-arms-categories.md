# Department of Agriculture: Search ARMS Categories

Finds ARMS categories in Department of Agriculture by ID or name.

```
GET https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/search-arms-categories
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Department of Agriculture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/search-arms-categories?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/search-arms-categories?${params}`, {
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
| `id` | string | no | Filter categories by ARMS category abbreviation. |
| `name` | string | no | Filter categories by category display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "abb": "string",
      "desc": "string",
      "element_Dim": [
        {}
      ],
      "header": "string",
      "seq": 1,
      "terms": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `abb` | string | Category abbreviation. |
| `desc` | string | Category description. |
| `element_Dim` | array<object> | Available values for the category. |
| `header` | string | Category name. |
| `seq` | number | Category sequence. |
| `terms` | string | Provider search terms. |

## Native endpoint

Through the native Department of Agriculture API, this operation is `GET /arms/category` (base URL `https://api.ers.usda.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-arms-categories.md) for the provider-specific parameters and requirements.

