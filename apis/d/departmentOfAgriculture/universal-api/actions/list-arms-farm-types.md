# Department of Agriculture: List ARMS Farm Types

Retrieves ARMS farm types from Department of Agriculture.

```
GET https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-farm-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Department of Agriculture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-farm-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-farm-types?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



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

Through the native Department of Agriculture API, this operation is `GET /arms/farmtype` (base URL `https://api.ers.usda.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-arms-farm-types.md) for the provider-specific parameters and requirements.

