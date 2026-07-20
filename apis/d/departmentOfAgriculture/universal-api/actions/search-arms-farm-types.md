# Department of Agriculture: Search ARMS Farm Types

Finds ARMS farm types in Department of Agriculture by ID or name.

```
GET https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/search-arms-farm-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Department of Agriculture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/search-arms-farm-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/search-arms-farm-types?${params}`, {
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
| `id` | number | no | Filter farm types by numeric ID. |
| `name` | string | no | Filter farm types by display name. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "header": "string",
      "invalid": true,
      "num": 1,
      "survey_Abb": "string",
      "terms": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string | Farm type description. |
| `header` | string | Farm type name. |
| `invalid` | boolean | Whether the farm type is invalid. |
| `num` | number | Farm type number. |
| `survey_Abb` | string | Associated survey abbreviation. |
| `terms` | string | Provider search terms. |

## Native endpoint

Through the native Department of Agriculture API, this operation is `GET /arms/farmtype` (base URL `https://api.ers.usda.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-arms-farm-types.md) for the provider-specific parameters and requirements.

