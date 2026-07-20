# Department of Agriculture: List ARMS Years

Retrieves ARMS survey years from Department of Agriculture.

```
GET https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-years
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Department of Agriculture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-years?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/departmentOfAgriculture/latest/actions/list-arms-years?${params}`, {
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
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | number | Available ARMS survey year. |

## Native endpoint

Through the native Department of Agriculture API, this operation is `GET /arms/year` (base URL `https://api.ers.usda.gov/data`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-arms-years.md) for the provider-specific parameters and requirements.

