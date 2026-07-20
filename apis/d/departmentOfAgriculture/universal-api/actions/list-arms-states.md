# Department of Agriculture: List ARMS States

Retrieves ARMS states from Department of Agriculture.

```
GET https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-states
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Department of Agriculture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-states?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-states?${params}`, {
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
      "code": "string",
      "id": "string",
      "name": "Ava Chen",
      "terms": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | State abbreviation or ALL code for all survey states. |
| `id` | string | USDA state/FIPS identifier. |
| `name` | string | State display name. |
| `terms` | string | Provider search terms, when available. |

## Native endpoint

Through the native Department of Agriculture API, this operation is `GET /arms/state` (base URL `https://api.ers.usda.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-arms-states.md) for the provider-specific parameters and requirements.

